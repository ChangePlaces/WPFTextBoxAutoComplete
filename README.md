WPFTextBoxAutoComplete
======================

An attached behavior for WPF's TextBox control that provides auto-completion suggestions from a given collection

## How to use this library:

* Install the package via NuGet

	PM> Install-Package WPFTextBoxAutoComplete

* Add a reference to the library in your view
	
	xmlns:behaviors="clr-namespace:WPFTextboxAutoComplete;assembly=WPFTextboxAutoComplete"
	
* Create a textbox and bind the "AutoCompleteItemsSource" to a collection if IEnumerable<String>
	
	<TextBox 
        Width="250"
        HorizontalAlignment="Center"
        Text="{Binding TestText, UpdateSourceTrigger=PropertyChanged}" 
        behaviors:AutoCompleteBehavior.AutoCompleteItemsSource="{Binding TestItems}" 
    />
    
Now, every time the "TestText" property of your datacontext is changed, WPFTextBoxAutoComplete will provide you with auto-completion suggestions.  To accept a suggestion, just hit "enter".

		
