

	<property name="custom:property1">
		<title>Property 1</title>
		<type>d:text</type>
		<mandatory>true</mandatory>
	</property>

	<property name="custom:property2">
		<title>Property 2</title>
		<type>d:text</type>
		<mandatory>true</mandatory>
	</property>

Into the share-config-custom.xml file, configure your custom type to something like this:

<config evaluator="node-type" condition="custom:customType">
	<forms>
		<form>
			<field-visibility>
				<show id="cm:name" />

				<!-- customProperties -->
				<show id="custom:property1" />
				<show id="custom:property2" />
			</field-visibility>
			<appearance>
				<field id="custom:property1">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 1 Datalist</control-param>
						<control-param name="level">1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
				<field id="custom:property2">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 2 Datalist</control-param>
						<control-param name="level">2</control-param>
						<control-param name="dependsOn">prop_custom_property1
						</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
			</appearance>
		</form>

		<!-- Document Library pop-up Edit Metadata form -->
		<form id="doclib-simple-metadata">
			<field-visibility>
				<show id="cm:name" />

				<!-- customProperties -->
				<show id="custom:property1" />
				<show id="custom:property2" />
			</field-visibility>
			<appearance>
				<field id="custom:property1">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 1 Datalist</control-param>
						<control-param name="level">1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
				<field id="custom:property2">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 2 Datalist</control-param>
						<control-param name="level">2</control-param>
						<control-param name="dependsOn">prop_custom_property1
						</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
			</appearance>
		</form>

		<!-- Document Library Inline Edit form -->
		<form id="doclib-inline-edit">
			<field-visibility>
				<show id="cm:name" />

				<!-- customProperties -->
				<show id="custom:property1" />
				<show id="custom:property2" />
			</field-visibility>
			<appearance>
				<field id="custom:property1">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 1 Datalist</control-param>
						<control-param name="level">1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
				<field id="custom:property2">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 2 Datalist</control-param>
						<control-param name="level">2</control-param>
						<control-param name="dependsOn">prop_custom_property1
						</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
			</appearance>
		</form>
	</forms>
</config>

<config evaluator="model-type" condition="custom:customType">
	<forms>
		<!-- Search form -->
		<form id="search">
			<field-visibility>
				<show id="cm:name" />

				<!-- customProperties -->
				<show id="custom:property1" force="true" />
				<show id="custom:property1" force="true" />
			</field-visibility>
			<appearance>
				<field id="custom:property1">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 1 Datalist</control-param>
						<control-param name="level">1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
				<field id="custom:property2">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 2 Datalist</control-param>
						<control-param name="level">2</control-param>
						<control-param name="dependsOn">prop_custom_property1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
			</appearance>
		</form>

		<!-- New documents -->
		<form>
			<field-visibility>
				<show id="cm:name" />

				<!-- customProperties -->
				<show id="custom:property1" />
				<show id="custom:property2" />
			</field-visibility>
			<appearance>
				<field id="custom:property1">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 1 Datalist</control-param>
						<control-param name="level">1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
				<field id="custom:property2">
					<control template="/form-controls/dynamic-dropdown.ftl">
						<control-param name="picklistName">Property 2 Datalist</control-param>
						<control-param name="level">2</control-param>
						<control-param name="dependsOn">prop_custom_property1</control-param>
						<control-param name="loadLabel">true</control-param>
					</control>
				</field>
			</appearance>
		</form>
	</forms>
</config>

