<template>
	<div class="content-section documentation">
		<TabView>
			<TabPanel header="Documentation">
				<h3>Import</h3>
<CodeHighlight lang="javascript">
import InputNumber from 'primevue/inputnumber';
</CodeHighlight>

<h3>Getting Started</h3>
            <p>InputNumber is used with the standard v-model directive. Component always provides a number type although formatting on the input is a string.</p>

<CodeHighlight>
&lt;InputNumber v-model="value" /&gt;
</CodeHighlight>

            <h3>Decimal Mode</h3>
            <p>Format is defined using the <i>mode</i> property, "decimal" is the default value allowing only integers when there is no other configuration.</p>
<CodeHighlight>
&lt;InputNumber v-model="value" mode="decimal" /&gt;
</CodeHighlight>

            <p>Fractions are configured with the <i>minFractionDigits</i> property. Optionally <i>maxFractionDigits</i> can be used to defined a boundary for the maximum digits.</p>
<CodeHighlight>
&lt;InputNumber v-model="value1" mode="decimal" :minFractionDigits="2" /&gt;
&lt;InputNumber v-model="value2" mode="decimal" :minFractionDigits="2" :maxFracionDigits="2" /&gt;
</CodeHighlight>

            <p><i>locale</i> option is available to set the localization information such as grouping and decimal symbols where default value is the browser locale. Locales are defined per <a href="https://tools.ietf.org/html/rfc5646">BCP Language Tag</a>.</p>
<CodeHighlight>
User Locale
&lt;InputNumber v-model="value1" mode="decimal" :minFractionDigits="2" /&gt;

United State Locale
&lt;InputNumber v-model="value2" mode="decimal" locale="en-US" :minFractionDigits="2" /&gt;

German Locale
&lt;InputNumber v-model="value3" mode="decimal" locale="de-DE" :minFractionDigits="2" /&gt;

Indian Locale
&lt;InputNumber v-model="value4" mode="decimal" locale="en-IN" :minFractionDigits="2" /&gt;
</CodeHighlight>

            <h3>Currency</h3>
            <p>Currency formatting is specified by setting the <i>mode</i> option to currency and <i>currency</i> property. In addition <i>currencyDisplay</i> option
            allows how the currency is displayed, valid values are "symbol" (default) or "code".</p>
<CodeHighlight>
United States
&lt;InputNumber v-model="value1" mode="currency" currency="USD" locale="en-US" /&gt;

Germany
&lt;InputNumber v-model="value2" mode="currency" currency="EUR" locale="de-DE" /&gt;

India
&lt;InputNumber v-model="value3" mode="currency" currency="INR" currencyDisplay="code" locale="en-IN" /&gt;

Japan
&lt;InputNumber v-model="value4" mode="currency" currency="JPY" locale="jp-JP" /&gt;
</CodeHighlight>

            <h3>Prefix and Suffix</h3>
            <p>Custom texts e.g. units can be placed before or after the input section with the <i>prefix</i> and <i>suffix</i> properties.</p>
<CodeHighlight>
Mile
&lt;InputNumber v-model="value1" suffix=" mi" /&gt;

Percent
&lt;InputNumber v-model="value2" prefix="%" /&gt;

Expiry
&lt;InputNumber v-model="value3" prefix="Expires in " suffix=" days" /&gt;

Temperature
&lt;InputNumber v-model="value4" prefix="&uarr; " suffix="℃" :min="0" :max="40" /&gt;
</CodeHighlight>

            <h3>Buttons</h3>
            <p>Spinner buttons is enabled using the <i>showButtons</i> options and layout is defined with the <i>buttonLayout</i>. Default value is "stacked" whereas
            "horizontal" and "stacked" are alternatives. Note that even there are no buttons, up and down arrow keys can be used to spin the values with keyboard.</p>
<CodeHighlight>
Stacked
&lt;InputNumber v-model="value1" showButtons mode="currency" currency="USD" /&gt;

Horizontal
&lt;InputNumber v-model="value2" showButtons buttonLayout="horizontal" spinnerMode="horizontal"
    decrementButtonClass="p-button-danger" incrementButtonClass="p-button-success" incrementButtonIcon="pi pi-plus" decrementButtonIcon="pi pi-minus" mode="currency" currency="EUR" /&gt;

Vertical
&lt;InputNumber v-model="value3" mode="decimal" showButtons buttonLayout="vertical" spinnerMode="vertical"
    decrementButtonClass="p-button-secondary" incrementButtonClass="p-button-secondary" incrementButtonIcon="pi pi-plus" decrementButtonIcon="pi pi-minus" /&gt;
</CodeHighlight>

            <h3>Step</h3>
            <p>Step factor is 1 by default and can be customized with <i>step</i> option.</p>
<CodeHighlight>
&lt;InputNumber v-model="value" :step="0.25" /&gt;
</CodeHighlight>


            <h3>Min and Max Boundaries</h3>
            <p>Value to be entered can be restricted by configuring the <i>min</i> and <i>max</i> options.</p>
<CodeHighlight>
&lt;InputNumber v-model="value" :min="0" :max="100" /&gt;
</CodeHighlight>


				<h3>Properties</h3>
				<p>InputNumber passes any valid attribute to the underlying input element.</p>
                <div className="doc-tablewrapper">
                    <table className="doc-table">
                        <thead>
                            <tr>
                                <th>Name</th>
                                <th>Type</th>
                                <th>Default</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>value</td>
                                <td>number</td>
                                <td>null</td>
                                <td>Value of the component.</td>
                            </tr>
                            <tr>
                                <td>format</td>
                                <td>boolean</td>
                                <td>true</td>
                                <td>Whether to format the value.</td>
                            </tr>
                            <tr>
                                <td>showButtons</td>
                                <td>boolean</td>
                                <td>false</td>
                                <td>Displays spinner buttons.</td>
                            </tr>
                            <tr>
                                <td>buttonLayout</td>
                                <td>string</td>
                                <td>stacked</td>
                                <td>Layout of the buttons, valid values are "stacked" (default), "horizontal" and "vertical".</td>
                            </tr>
                            <tr>
                                <td>incrementButtonClassName</td>
                                <td>string</td>
                                <td>null</td>
                                <td>Style class of the increment button.</td>
                            </tr>
                            <tr>
                                <td>decrementButtonClassName</td>
                                <td>string</td>
                                <td>null</td>
                                <td>Style class of the decrement button.</td>
                            </tr>
                            <tr>
                                <td>incrementButtonIcon</td>
                                <td>string</td>
                                <td>pi pi-caret-up</td>
                                <td>Style class of the increment button.</td>
                            </tr>
                            <tr>
                                <td>decrementButtonIcon</td>
                                <td>string</td>
                                <td>pi pi-caret-down</td>
                                <td>Style class of the decrement button.</td>
                            </tr>
                            <tr>
                                <td>locale</td>
                                <td>string</td>
                                <td>null</td>
                                <td>Locale to be used in formatting.</td>
                            </tr>
                            <tr>
                                <td>localeMatcher</td>
                                <td>string</td>
                                <td>best fit</td>
                                <td>The locale matching algorithm to use. Possible values are "lookup" and "best fit"; the default is "best fit".
                                    See <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl#Locale_negotiation">Locale Negotation</a> for details.
                                </td>
                            </tr>
                            <tr>
                                <td>mode</td>
                                <td>string</td>
                                <td>decimal</td>
                                <td>Defines the behavior of the component, valid values are "decimal" and "currency".</td>
                            </tr>
                            <tr>
                                <td>prefix</td>
                                <td>string</td>
                                <td>null</td>
                                <td>Text to display before the value.</td>
                            </tr>
                            <tr>
                                <td>suffix</td>
                                <td>string</td>
                                <td>decimal</td>
                                <td>Text to display after the value.</td>
                            </tr>
                            <tr>
                                <td>currency</td>
                                <td>string</td>
                                <td>null</td>
                                <td>The currency to use in currency formatting. Possible values are the <a href="https://www.currency-iso.org/en/home/tables/table-a1.html">ISO 4217 currency codes</a>,
                                    such as "USD" for the US dollar, "EUR" for the euro, or "CNY" for the Chinese RMB.
                                    There is no default value; if the style is "currency", the currency property must be provided.</td>
                            </tr>
                            <tr>
                                <td>currencyDisplay</td>
                                <td>string</td>
                                <td>symbol</td>
                                <td>How to display the currency in currency formatting. Possible values are "symbol" to use a localized currency symbol such as €,
                                    ü"code" to use the ISO currency code, "name" to use a localized currency name such as "dollar"; the default is "symbol".</td>
                            </tr>
                            <tr>
                                <td>useGrouping</td>
                                <td>boolean</td>
                                <td>true</td>
                                <td>Whether to use grouping separators, such as thousands separators or thousand/lakh/crore separators.</td>
                            </tr>
                            <tr>
                                <td>minFractionDigits</td>
                                <td>number</td>
                                <td>null</td>
                                <td>The minimum number of fraction digits to use. Possible values are from 0 to 20; the default for plain number and percent formatting is 0; the default for currency formatting is the number of
                                    minor unit digits provided by the <a href="https://www.currency-iso.org/en/home/tables/table-a1.html">ISO 4217 currency code list</a> (2 if the list doesn't provide that information).</td>
                            </tr>
                            <tr>
                                <td>maxFractionDigits</td>
                                <td>number</td>
                                <td>null</td>
                                <td>The maximum number of fraction digits to use. Possible values are from 0 to 20; the default for plain
                                    number formatting is the larger of minimumFractionDigits and 3; the default for currency formatting
                                    is the larger of minimumFractionDigits and the number of minor unit digits provided by the <a href="https://www.currency-iso.org/en/home/tables/table-a1.html">ISO 4217 currency code list</a>
                                    (2 if the list doesn't provide that information).</td>
                            </tr>
                            <tr>
                                <td>min</td>
                                <td>number</td>
                                <td>null</td>
                                <td>Mininum boundary value.</td>
                            </tr>
                            <tr>
                                <td>max</td>
                                <td>number</td>
                                <td>null</td>
                                <td>Maximum boundary value.</td>
                            </tr>
                            <tr>
                                <td>step</td>
                                <td>number</td>
                                <td>1</td>
                                <td>Step factor to increment/decrement the value.</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <h3>Events</h3>
                <p>Any valid event such as focus, blur and input are passed to the underlying input element.</p>

				<h3>Styling</h3>
				<p>Following is the list of structural style classes, for theming classes visit <router-link to="/theming">theming</router-link> page.</p>
				<div class="doc-tablewrapper">
					<table class="doc-table">
						<thead>
                            <tr>
                                <th>Name</th>
                                <th>Element</th>
                            </tr>
						</thead>
						<tbody>
                            <tr>
                                <td>p-inputnumber</td>
                                <td>Container element</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-stacked</td>
                                <td>Container element with stacked buttons.</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-horizontal</td>
                                <td>Container element with horizontal buttons.</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-vertical</td>
                                <td>Container element with vertical buttons.</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-input</td>
                                <td>Input element</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-button</td>
                                <td>Input element</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-button-up</td>
                                <td>Increment button</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-button-down</td>
                                <td>Decrement button</td>
                            </tr>
                            <tr>
                                <td>p-inputnumber-button-icon</td>
                                <td>Button icon</td>
                            </tr>
						</tbody>
					</table>
				</div>

				<h3>Dependencies</h3>
				<p>None.</p>
			</TabPanel>

			<TabPanel header="Source">
				<a href="https://github.com/primefaces/primevue/tree/master/src/views/inputtext" class="btn-viewsource" target="_blank" rel="noopener noreferrer">
					<span>View on GitHub</span>
				</a>
<CodeHighlight>
<template v-pre>
&lt;h3&gt;Numerals&lt;/h3&gt;
&lt;div class="p-grid p-fluid"&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Integer Only
        &lt;InputNumber v-model="value1" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Without Grouping
        &lt;InputNumber v-model="value2" mode="decimal" :useGrouping="false" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Min-Max Fraction Digits
        &lt;InputNumber v-model="value3" mode="decimal" :minFractionDigits="2" :maxFractionDigits="5" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Min-Max Boundaries
        &lt;InputNumber v-model="value4" mode="decimal" :min="0" :max="100" /&gt;
    &lt;/div&gt;

    &lt;div class="p-col-12 p-md-3"&gt;
        User Locale
        &lt;InputNumber v-model="value5" mode="decimal" :minFractionDigits="2" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        United State Locale
        &lt;InputNumber v-model="value6" mode="decimal" locale="en-US" :minFractionDigits="2" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        German Locale
        &lt;InputNumber v-model="value7" mode="decimal" locale="de-DE" :minFractionDigits="2"/&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Indian Locale
        &lt;InputNumber v-model="value8" mode="decimal" locale="en-IN" :minFractionDigits="2" /&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;h3&gt;Currency&lt;/h3&gt;
&lt;div class="p-grid p-fluid"&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        United States
        &lt;InputNumber v-model="value9" mode="currency" currency="USD" locale="en-US" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Germany
        &lt;InputNumber v-model="value10" mode="currency" currency="EUR" locale="de-DE" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        India
        &lt;InputNumber v-model="value11" mode="currency" currency="INR" currencyDisplay="code" locale="en-IN" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Japan
        &lt;InputNumber v-model="value12" mode="currency" currency="JPY" locale="jp-JP" /&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;h3&gt;Prefix and Suffix&lt;/h3&gt;
&lt;div class="p-grid p-fluid"&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Mile
        &lt;InputNumber v-model="value13" suffix=" mi" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Percent
        &lt;InputNumber v-model="value14" prefix="%" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Expiry
        &lt;InputNumber v-model="value15" prefix="Expires in " suffix=" days" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Temperature
        &lt;InputNumber v-model="value16" prefix="&uarr; " suffix="℃" :min="0" :max="40" /&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;h3&gt;Buttons&lt;/h3&gt;
&lt;div class="p-grid p-fluid"&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Stacked
        &lt;InputNumber v-model="value17" showButtons mode="currency" currency="USD" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Horizontal with Step
        &lt;InputNumber v-model="value18" showButtons buttonLayout="horizontal" spinnerMode="horizontal" :step="0.25"
            decrementButtonclass="p-button-danger" incrementButtonclass="p-button-success" incrementButtonIcon="pi pi-plus" decrementButtonIcon="pi pi-minus" mode="currency" currency="EUR" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        &lt;div&gt;Vertical&lt;/div&gt;
        &lt;InputNumber v-model="value19" mode="decimal" showButtons buttonLayout="vertical" spinnerMode="vertical"
            decrementButtonClass="p-button-secondary" incrementButtonClass="p-button-secondary" incrementButtonIcon="pi pi-plus" decrementButtonIcon="pi pi-minus" /&gt;
    &lt;/div&gt;
    &lt;div class="p-col-12 p-md-3"&gt;
        Min-Max Boundaries
        &lt;InputNumber v-model="value20" mode="decimal" showButtons :min="0" :max="100" /&gt;
    &lt;/div&gt;
&lt;/div&gt;
</template>
</CodeHighlight>

<CodeHighlight lang="javascript">
export default {
    data() {
        return {
            value1: 42723,
            value2: 58151,
            value3: 2351.35,
            value4: 50,
            value5: 151351,
            value6: 115744,
            value7: 635524,
            value8: 732762,
            value9: 1500,
            value10: 2500,
            value11: 4250,
            value12: 5002,
            value13: 20,
            value14: 50,
            value15: 10,
            value16: 20,
            value17: 20,
            value18: 10.50,
            value19: 25,
            value20: 50
        }
    }
}
</CodeHighlight>
			</TabPanel>
		</TabView>
	</div>
</template>