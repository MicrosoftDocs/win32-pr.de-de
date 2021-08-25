---
title: Eigenschaftenbezeichner für Automation-Elemente (UIAutomationClient.h)
description: In diesem Thema werden die benannten Konstanten beschrieben, die die Eigenschaften von Microsoft Benutzeroberflächenautomatisierung-Elementen identifizieren.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b373091ec34e71afbac32fca962ec380513acfcd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627696"
---
# <a name="automation-element-property-identifiers"></a>Automation-Elementeigenschaftenbezeichner

In diesem Thema werden die benannten Konstanten beschrieben, die die Eigenschaften von Microsoft Benutzeroberflächenautomatisierung-Elementen identifizieren.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Konstante/Wert</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td >Identifiziert die <strong>AcceleratorKey-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die die Tastenkombinationen (auch als Tastenkombination bezeichnet) für das Automatisierungselement enthält. <br/> Tastenkombinationen rufen eine Aktion auf. Strg+O wird z. B. häufig verwendet, um das Dialogfeld Datei öffnen häufig aufzurufen. Ein Automatisierungselement mit der <strong>AcceleratorKey-Eigenschaft</strong> kann das <a href="uiauto-implementinginvoke.md">Invoke-Steuerelementmuster</a> für die Aktion implementieren, die dem Verknüpfungsbefehl entspricht.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td >Identifiziert die <strong>AccessKey-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die das Zugriffsschlüsselzeichen für das Automation-Element enthält.<br/> Ein Zugriffsschlüssel (manchmal auch als mnemonic bezeichnet) ist ein Zeichen im Text eines Menüs, eines Menüelements oder einer Bezeichnung eines Steuerelements, z. B. einer Schaltfläche, das die zugeordnete Menüfunktion aktiviert. Um z. B. das Menü Datei zu öffnen, für das die Zugriffstaste in der Regel F lautet, würde der Benutzer ALT+F drücken.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td >Identifiziert die <strong>AnnotationObjects-Eigenschaft,</strong> bei der es sich um eine Liste von Anmerkungsobjekten in einem Dokument handelt, z. B. Kommentar, Kopfzeile, Fußzeile usw.<br/> Variantentyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td >Identifiziert die <strong>AnnotationTypes-Eigenschaft,</strong> bei der es sich um eine Liste der Typen von Anmerkungen in einem Dokument handelt, z. B. Kommentar, Kopfzeile, Fußzeile usw.<br/> Variantentyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td >Identifiziert die <strong>AriaProperties-Eigenschaft,</strong> bei der es sich um eine formatierte Zeichenfolge handelt, die die ARIA-Eigenschafteninformationen (Accessible Rich Internet Application) für das Automation-Element enthält. Weitere Informationen zum Zuordnen von ARIA-Zuständen und -Eigenschaften zu Benutzeroberflächenautomatisierung Eigenschaften und Funktionen finden Sie unter <a href="uiauto-ariaspecification.md">Benutzeroberflächenautomatisierung for W3C Accessible Rich Internet Applications Specification (W3C Accessible Rich Internet Applications Specification).</a><br/> <strong>AriaProperties</strong> ist eine Auflistung von Name-Wert-Paaren mit Trennzeichen von <strong>=</strong> (equals) und <strong>;</strong> (Semikolon), z.B. &quot; checked=true;disabled=false. &quot; Der <strong>\</strong> (umgekehrte Schrägstrich) wird als Escapezeichen verwendet, wenn diese Trennzeichen oder <strong>\</strong> in den Werten angezeigt werden. Aus Sicherheits- und anderen Gründen kann die Anbieterimplementierungen dieser Eigenschaft Schritte ausführen, um die ursprünglichen ARIA-Eigenschaften zu überprüfen. dies ist jedoch nicht erforderlich.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td >Identifiziert die <strong>AriaRole-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die die ARIA-Rolleninformationen (Accessible Rich Internet Application) für das Automation-Element enthält. Weitere Informationen zum Zuordnen von ARIA-Rollen zu Benutzeroberflächenautomatisierung Steuerelementtypen finden Sie unter <a href="uiauto-ariaspecification.md">Benutzeroberflächenautomatisierung für W3C Accessible Rich Internet Applications Specification ( W3C Accessible Rich Internet Applications Specification).</a><br/>
<blockquote>
[!Note]<br />
Optional kann der Benutzer-Agent auch eine lokalisierte Beschreibung der W3C-ARIA-Rolle in der <strong>LocalizedControlType-Eigenschaft</strong> anbieten. Wenn die lokalisierte Zeichenfolge nicht angegeben ist, stellt das System die Standardmäßige <strong>LocalizedControlType-Zeichenfolge</strong> für das Element bereit.
</blockquote>
<br/> <br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td >Identifiziert die <strong>AutomationId-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die den Benutzeroberflächenautomatisierung Bezeichner (ID) für das Automation-Element enthält.<br/> Wenn sie verfügbar ist, muss die <strong>AutomationId</strong> eines Elements in jeder Instanz der Anwendung unabhängig von der lokalen Sprache identisch sein. Der Wert sollte für gleichgeordnete Elemente eindeutig sein, aber nicht notwendigerweise für den gesamten Desktop. Beispielsweise können mehrere Instanzen einer Anwendung oder mehrere Ordneransichten in Microsoft Windows Explorer Elemente mit derselben <strong>AutomationId-Eigenschaft</strong> enthalten, z. B. &quot; SystemMenuBar. &quot;<br/> Obwohl die Unterstützung für <strong>AutomationId</strong> immer für eine bessere Unterstützung automatisierter Tests empfohlen wird, ist diese Eigenschaft nicht obligatorisch. Wo sie unterstützt wird, ist <strong>AutomationId</strong> nützlich zum Erstellen eines Testautomatisierungsskripts, das unabhängig von der Benutzeroberflächensprache ausgeführt wird. Clients sollten keine Annahmen hinsichtlich der <strong>AutomationId-Werte</strong> treffen, die von anderen Anwendungen verfügbar gemacht werden. Es ist nicht garantiert, dass <strong>AutomationId</strong> in verschiedenen Releases oder Builds einer Anwendung stabil ist.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td >Identifiziert die <strong>BoundingRectangle-Eigenschaft,</strong> die die Koordinaten des Rechtecks angibt, das das Automatisierungselement vollständig einschließt. Das Rechteck wird in physischen Bildschirmkoordinaten ausgedrückt. Er kann Punkte enthalten, auf die nicht geklickt werden kann, wenn die Form oder der klickbare Bereich des Ui-Elements unregelmäßig ist oder wenn das Element von anderen Benutzeroberflächenelementen verdeckt wird.<br/> Variantentyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: [0,0,0,0]<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft ist <strong>NULL,</strong> wenn das Element derzeit keine Benutzeroberfläche anzeigt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td >Identifiziert die <strong>CenterPoint-Eigenschaft,</strong> die die mittleren X- und Y-Punktkoordinaten des Automatisierungselements angibt. Der Koordinatenraum wird vom Anbieter logisch als Seite betrachtet.<br/> Variantentyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td >Identifiziert die <strong>ClassName-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die den Klassennamen für das Automatisierungselement enthält, wie vom Steuerelemententwickler zugewiesen.<br/> Der Klassenname hängt von der Implementierung des Benutzeroberflächenautomatisierung-Anbieters ab und weist daher nicht immer ein Standardformat auf. Wenn der Klassenname jedoch bekannt ist, kann er verwendet werden, um zu überprüfen, ob eine Anwendung mit dem erwarteten Automatisierungselement arbeitet.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td >Identifiziert die <strong>ClickablePoint-Eigenschaft,</strong> die ein Punkt auf dem Automatisierungselement ist, auf das geklickt werden kann. Auf ein Element kann nicht geklickt werden, wenn es von einem anderen Fenster vollständig oder teilweise verdeckt wird.<br/> Variantentyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td >Identifiziert die <strong>ControllerFor-Eigenschaft,</strong> bei der es sich um ein Array von Automatisierungselementen handelt, die vom Automatisierungselement bearbeitet werden, das diese Eigenschaft unterstützt.<br/> <strong>ControllerFor</strong> wird verwendet, wenn sich ein Automatisierungselement auf ein oder mehrere Segmente der Anwendungsoberfläche oder des Desktops auswirkt. Andernfalls ist es schwierig, die Auswirkungen des Steuerelementvorgangs ui-Elementen zuzuordnen.<br/> Dieser Bezeichner wird häufig für <a href="/windows/uwp/design/accessibility/accessible-text-requirements">die automatische Barrierefreiheit</a>verwendet.<br/> Variantentyp für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Variantentyp für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td >Identifiziert die <strong>ControlType-Eigenschaft,</strong> bei der es sich um eine Klasse handelt, die den Typ des Automatisierungselements identifiziert. <strong>ControlType</strong> definiert Merkmale der Benutzeroberflächenelemente durch bekannte Grundtypen von UI-Steuerelementen wie Schaltflächen oder Kontrollkästchen. <br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Verwenden Sie den Standardwert nur, wenn das Automatisierungselement einen völlig neuen Steuerelementtyp darstellt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td >Identifiziert die <strong>Culture-Eigenschaft,</strong> die einen Gebietsschemabezeichner für das Automatisierungselement enthält (z. B. <code>0x0409</code> für &quot; en-US &quot; oder Englisch (USA)).<br/> Jedes Gebietsschema verfügt über einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einem Sprachbezeichner und einem Sortierreihenfolgebezeichner besteht. Der Gebietsschemabezeichner ist eine standardmäßige internationale numerische Abkürzung und verfügt über die Komponenten, die erforderlich sind, um eines der vom Betriebssystem definierten Gebietsschemas eindeutig zu identifizieren. Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Sprachbezeichnerkonstanten und Zeichenfolgen.</a><br/> Diese Eigenschaft kann auf Steuerungsbasis vorhanden sein, ist jedoch in der Regel nur auf Anwendungsebene verfügbar.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td >Identifiziert die <strong>DescribedBy-Eigenschaft,</strong> bei der es sich um ein Array von Elementen handelt, die weitere Informationen zum Automatisierungselement bereitstellen.<br/> <strong>DescribedBy</strong> wird verwendet, wenn ein Automatisierungselement durch ein anderes Segment der Anwendungsbenutzeroberfläche erklärt wird. Beispielsweise kann die -Eigenschaft auf ein Textelement mit &quot; 2.529 Elementen in 85 Gruppen verweisen, 10 Elemente, die aus einem komplexen benutzerdefinierten &quot; Listenobjekt ausgewählt wurden. Anstatt das Objektmodell für Clients zu verwenden, um ähnliche Informationen zu verarbeiten, kann die <strong>DescribedBy-Eigenschaft</strong> schnellen Zugriff auf das Benutzeroberflächenelement bieten, das möglicherweise bereits nützliche Endbenutzerinformationen enthält, die das Benutzeroberflächenelement beschreiben.<br/> Variant-Typ für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Variant-Typ für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td >Identifiziert die <strong>FillColor-Eigenschaft,</strong> die die Farbe angibt, die zum Füllen des Automatisierungselements verwendet wird. Dieses Attribut wird als COLORREF angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td >Identifiziert die <strong>FillType-Eigenschaft,</strong> die das Muster angibt, mit dem das Automatisierungselement gefüllt wird, z. B. none, color, gradient, picture, pattern und so weiter.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td >Identifiziert die <strong>FlowsFrom-Eigenschaft,</strong> bei der es sich um ein Array von Automatisierungselementen handelt, das die Lese reihenfolge vor dem aktuellen Automatisierungselement vorschlägt. Unterstützt ab Windows 8.<br/> Die <strong>FlowsFrom-Eigenschaft</strong> gibt die Lese reihenfolge an, wenn Automatisierungselemente nicht in derselben Lese reihenfolge verfügbar gemacht oder strukturiert werden, wie sie vom Benutzer wahrgenommen wird. Während die <strong>FlowsFrom-Eigenschaft</strong> mehrere vorangehende Elemente angeben kann, enthält sie in der Regel nur das vorherige Element in der Lesefolge.<br/> Variant-Typ für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Variant-Typ für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td >Identifiziert die <strong>FlowsTo-Eigenschaft,</strong> bei der es sich um ein Array von Automatisierungselementen handelt, das die Lese reihenfolge nach dem aktuellen Automatisierungselement vorschlägt.<br/> Die <strong>FlowsTo-Eigenschaft</strong> gibt die Lese reihenfolge an, wenn Automatisierungselemente nicht in derselben Lese reihenfolge verfügbar gemacht oder strukturiert werden, die vom Benutzer wahrgenommen wird. Während die <strong>FlowsTo-Eigenschaft</strong> mehrere elemente angeben kann, die erfolgreich sind, enthält sie in der Regel nur das nächste Element in der Lese reihenfolge.<br/> Variant-Typ für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Variant-Typ für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td >Identifiziert die <strong>FrameworkId-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die den Namen des zugrunde liegenden Benutzeroberflächenframework enthält, zu dem das Automatisierungselement gehört.<br/> Mit <strong>der FrameworkId</strong> können Clientanwendungen Automatisierungselemente abhängig vom jeweiligen Benutzeroberflächenframework unterschiedlich verarbeiten. Beispiele für Eigenschaftswerte sind &quot; Win32, &quot; &quot; WinForm &quot; und &quot; &quot; DirectUI.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td >Die <strong>FullDescription-Eigenschaft</strong> macht eine lokalisierte Zeichenfolge verfügbar, die erweiterten Beschreibungstext für ein Element enthalten kann. <strong>FullDescription</strong> kann eine vollständigere Beschreibung eines Elements enthalten, als für das Element Name geeignet <strong>ist.</strong><br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td >Identifiziert die <strong>HasKeyboardFocus-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungselement den Tastaturfokus besitzt.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td >Identifiziert die <strong>HeadingLevel-Eigenschaft,</strong> die die Überschriftenebene eines Benutzeroberflächenautomatisierung angibt.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td >Identifiziert die <strong>HelpText-Eigenschaft,</strong> bei der es sich um eine Hilfetextzeichenfolge handelt, die dem Automatisierungselement zugeordnet ist.<br/> Die <strong>HelpText-Eigenschaft</strong> kann mit Platzhaltertext unterstützt werden, der in Bearbeitungs- oder Listensteuerelementen angezeigt wird. Beispiel: Text hier für die Suche eingeben ist ein guter Kandidat für die &quot; HelpText-Eigenschaft für ein Bearbeitungssteuerfeld, das den Text vor der tatsächlichen &quot; Eingabe des Benutzers platziert. <strong></strong> Sie ist jedoch nicht für die Name-Eigenschaft des Bearbeitungssteuer steuerelements geeignet.<br/> Wenn <strong>HelpText unterstützt</strong> wird, muss die Zeichenfolge mit der Benutzeroberflächensprache der Anwendung oder der Standardsprache der Benutzeroberfläche des Betriebssystems übereinstimmen.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td >Identifiziert die <strong>IsContentElement-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Element in der Inhaltsansicht der Automatisierungselementstruktur angezeigt wird. Weitere Informationen finden Sie unter <a href="uiauto-treeoverview.md">Benutzeroberflächenautomatisierung Strukturübersicht.</a><br/>
<blockquote>
[!Note]<br />
Damit ein Element in der Inhaltsansicht angezeigt wird, müssen sowohl die <strong>IsContentElement-Eigenschaft</strong> als auch die <strong>IsControlElement-Eigenschaft</strong> <strong>TRUE sein.</strong>
</blockquote>
<br/> <br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>TRUE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td >Identifiziert die <strong>IsControlElement-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Element in der Steuerelementansicht der Automatisierungselementstruktur angezeigt wird. Weitere Informationen finden Sie unter <a href="uiauto-treeoverview.md">Benutzeroberflächenautomatisierung Strukturübersicht.</a><br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>TRUE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td >Identifiziert die <strong>IsDataValidForForm-Eigenschaft.</strong> Dies ist ein boolescher Wert, der angibt, ob der eingegebene oder ausgewählte Wert für die Formularregel gültig ist, die dem Automatisierungselement zugeordnet ist. Wenn der Benutzer beispielsweise 425-555-5555 für ein Postleitzahlfeld eingegeben hat, das 5 oder 9 Ziffern erfordert, kann die &quot; &quot; <strong>IsDataValidForForm-Eigenschaft</strong> auf <strong>FALSE</strong> festgelegt werden, um anzugeben, dass die Daten ungültig sind.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>

<tr class="odd">
<td ><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td >Identifiziert die <strong>IsDialog-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungselement ein Dialogfeld ist. Hilfstechnologie wie Sprachlesegeräte sprechen in der Regel den Titel des Dialogs, das fokussierte Steuerelement im Dialogfeld und dann den Inhalt des Dialogs bis zum fokussierten Steuerelement ( Möchten Sie Ihre Änderungen speichern, bevor Sie &quot; &quot; schließen). Bei Standardfenstern spricht eine Sprachausgabe in der Regel den Fenstertitel gefolgt vom fokussierten Steuerelement. Die <strong>IsDialog-Eigenschaft</strong> kann auf <strong>TRUE</strong> festgelegt werden, um anzugeben, dass die Clientanwendung das Element als Dialogfeld behandeln soll.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>

<tr class="even">
<td ><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td >Identifiziert die <strong>IsEnabled-Eigenschaft.</strong> Dies ist ein boolescher Wert, der angibt, ob das Benutzeroberflächenelement, auf das das Automatisierungselement verweist, aktiviert ist und mit dem interagiert werden kann.<br/> Wenn der aktivierte Zustand eines Steuerelements <strong>FALSE ist,</strong>wird davon ausgegangen, dass untergeordnete Steuerelemente ebenfalls nicht aktiviert sind. Clients sollten keine durch Eigenschaften geänderten Ereignisse von untergeordneten Elementen erwarten, wenn sich der Zustand des übergeordneten Steuerelements ändert.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td >Identifiziert die <strong>IsKeyboardFocusable-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungselement den Tastaturfokus akzeptieren kann.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td >Identifiziert die <strong>IsOffscreen-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungselement vollständig außerhalb der Ansicht gescrollt wird (z. B. ein Element in einem Listenfeld, das sich außerhalb des Viewports des Containerobjekts befindet) oder nicht mehr angezeigt wird (z. B. ein Element in einer Strukturansicht oder im Menü oder in einem minimierten Fenster). Wenn das Element über einen klickbaren Punkt verfügt, der dazu führen kann, dass es den Fokus erhält, wird das Element als auf dem Bildschirm angezeigt betrachtet, während ein Teil des Elements nicht auf dem Bildschirm angezeigt wird.<br/> Der Wert der -Eigenschaft wird nicht von der Verdecken durch andere Fenster oder davon beeinflusst, ob das Element auf einem bestimmten Monitor sichtbar ist.<br/> Wenn die <strong>IsOffscreen-Eigenschaft</strong> <strong>TRUE ist,</strong>wird das Benutzeroberflächenelement vom Bildschirm aus gescrollt oder reduziert. Das Element ist vorübergehend ausgeblendet, verbleibt jedoch in der Wahrnehmung des Endbenutzers und wird weiterhin in das Benutzeroberflächenmodell aufgenommen. Das Objekt kann durch Scrollen, Klicken auf eine Dropdownliste und so weiter wieder angezeigt werden.<br/> Objekte, die der Endbenutzer überhaupt nicht wahrnimmt oder die programmgesteuert ausgeblendet sind (z. B. ein Dialogfeld, das verworfen wurde, aber das zugrunde liegende Objekt weiterhin von der Anwendung zwischengespeichert wird), sollten sich nicht in der Automatisierungselementstruktur befinden (anstatt den Status von &quot; &quot; <strong>IsOffscreen</strong> auf <strong>TRUE</strong>zu setzen).<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td >Identifiziert die <strong>IsPassword-Eigenschaft.</strong> Dies ist ein boolescher Wert, der angibt, ob das Automatisierungselement geschützten Inhalt oder ein Kennwort enthält.<br/> Wenn die <strong>IsPassword-Eigenschaft</strong> <strong>TRUE ist</strong> und das Element den Tastaturfokus besitzt, sollte eine Clientanwendung das Tastaturfeedback oder Tastatureingabefeedback deaktivieren, das die geschützten Informationen des Benutzers verfügbar machen kann. Der Versuch, auf die <strong>Value-Eigenschaft</strong> des geschützten Elements (Bearbeitungssteuerelement) zu zugreifen, kann zu einem Fehler führen.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td >Identifiziert die <strong>IsPeripheral-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungselement die Peripheriebenutzeroberfläche darstellt. Die Benutzeroberfläche für Peripheriegeräte wird angezeigt und unterstützt die Benutzerinteraktion, nimmt jedoch den Tastaturfokus nicht ein, wenn sie angezeigt wird. Beispiele für die Peripheriebenutzeroberfläche sind Popups, Flyouts, Kontextmenüs oder unverankerte Benachrichtigungen. Unterstützt ab Windows 8.1.<br/> Wenn die <strong>IsPeripheral-Eigenschaft</strong> <strong>TRUE</strong>ist, kann eine Clientanwendung nicht davon ausgehen, dass der Fokus vom Element übernommen wurde, auch wenn es derzeit tastaturaktiv ist.<br/> Diese Eigenschaft ist für diese Steuerelementtypen relevant:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td >Identifiziert die <strong>IsRequiredForForm-Eigenschaft.</strong> Dies ist ein boolescher Wert, der angibt, ob das Automatisierungselement in einem Formular ausgefüllt werden muss.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td >Identifiziert die <strong>ItemStatus-Eigenschaft,</strong> bei der es sich um eine Textzeichenfolge handelt, die den Status eines Elements des Automatisierungselements beschreibt.<br/> <strong>Mit ItemStatus</strong> kann ein Client ermitteln, ob ein Element den Status eines Elements übermittelt und wie der Status ist. Ein Element, das einem Kontakt in einer Messaginganwendung zugeordnet ist, kann beispielsweise &quot; Ausgelastet &quot; oder &quot; Verbunden &quot; sein.<br/> Wenn <strong>ItemStatus unterstützt</strong> wird, muss die Zeichenfolge mit der Benutzeroberflächensprache der Anwendung oder der Standardsprache der Benutzeroberfläche des Betriebssystems übereinstimmen.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td >Identifiziert die <strong>ItemType-Eigenschaft,</strong> bei der es sich um eine Textzeichenfolge handelt, die den Typ des Automatisierungselements beschreibt.<br/> <strong>ItemType</strong> wird verwendet, um Informationen zu Elementen in einer Liste, Strukturansicht oder einem Datenraster zu erhalten. Beispielsweise kann ein Element in einer Dateiverzeichnisansicht eine &quot; Dokumentdatei oder &quot; ein Ordner &quot; &quot; sein.<br/> Wenn <strong>ItemType</strong> unterstützt wird, muss die Zeichenfolge mit der Benutzeroberflächensprache der Anwendung oder der Standardsprache der Benutzeroberfläche des Betriebssystems übereinstimmen.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td >Identifiziert die <strong>LabeledBy-Eigenschaft,</strong> bei der es sich um ein Automatisierungselement handelt, das die Textbezeichnung für dieses Element enthält.<br/> Diese Eigenschaft kann verwendet werden, um beispielsweise die statische Textbezeichnung für ein Kombinationsfeld abzurufen.<br/> Variant-Typ: <strong>VT_UNKNOWN</strong><br/> Standardwert: <strong>NULL</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td >Identifiziert die <strong>LandmarkType-Eigenschaft,</strong> bei der es sich um einen einem Element zugeordneten <a href="landmark-type-identifiers.md"><strong>Landmark-Typbezeichner</strong></a> handelt.<br/> Die <strong>LandmarkType-Eigenschaft</strong> beschreibt ein Element, das eine Gruppe von Elementen darstellt. Ein Suchdenkmal könnte z. B. einen Satz verwandter Steuerelemente für die Suche darstellen.<br/> Wenn <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> verwendet wird, ist <strong>UIA_LocalizedLandmarkTypePropertyId</strong> erforderlich, um das benutzerdefinierte Sehenswürdigkeit zu beschreiben.<br/> Variantentyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td >Identifiziert die <strong>Level-Eigenschaft,</strong> bei der es sich um eine 1-basierte ganze Zahl handelt, die einem Automatisierungselement zugeordnet ist.<br/> Die <strong>Level-Eigenschaft</strong> beschreibt die Position eines Elements in einer hierarchischen oder fehlerhaften hierarchischen Struktur. Beispielsweise können eine Aufzählung/Nummerierte Liste, Überschriften oder andere strukturierte Datenelemente unterschiedliche Beziehungen zwischen übergeordneten und untergeordneten Elementen haben. <strong>Level</strong> beschreibt, wo sich das Element in der Struktur befindet.<br/> Es wird empfohlen, das <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">CustomNavigation-Steuerelementmuster</a> zusammen mit Level zu <strong>verwenden.</strong><br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td >Identifiziert die <strong>LiveSetting-Eigenschaft,</strong> die von einem Automatisierungselement unterstützt wird, das einen Livebereich darstellt. Die <strong>LiveSetting-Eigenschaft</strong> gibt den Grad der Freundlichkeit an, den ein Client verwenden soll, um den Benutzer über Änderungen am &quot; &quot; Livebereich zu benachrichtigen. Diese Eigenschaft kann einer der Werte aus der <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting-Enumeration</strong></a> sein. Unterstützt ab Windows 8.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td >Identifiziert die <strong>LocalizedControlType-Eigenschaft,</strong> bei der es sich um eine Textzeichenfolge handelt, die den Typ des Steuerelements beschreibt, das das Automatisierungselement darstellt. Die Zeichenfolge sollte nur Kleinbuchstaben enthalten:
<ul>
<li>Richtig: &quot; Schaltfläche&quot;</li>
<li>Falsch: &quot; Schaltfläche&quot;</li>
</ul>
<br/> Wenn <strong>LocalizedControlType</strong> nicht vom Elementanbieter angegeben wird, wird die lokalisierte Standardzeichenfolge vom Framework entsprechend dem Steuerelementtyp des Elements bereitgestellt (z. B. Schaltfläche für den &quot; &quot; Button-Steuerelementtyp). <a href="uiauto-supportbuttoncontroltype.md"></a> Ein <strong></strong> &quot; Automatisierungselement mit dem Benutzerdefinierten Steuerelementtyp muss eine lokalisierte Steuerelementtypzeichenfolge unterstützen, die die Rolle des Elements darstellt (z. B. Farbauswahl für ein benutzerdefiniertes Steuerelement, mit dem Benutzer Farben auswählen und angeben &quot; können).<br/> Wenn ein benutzerdefinierter Wert angegeben wird, muss die Zeichenfolge mit der Benutzeroberflächensprache der Anwendung oder der Standardsprache der Benutzeroberfläche des Betriebssystems übereinstimmen.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td >Identifiziert <strong>localizedLandmarkType,</strong>eine Textzeichenfolge, die den Typ des Orientierungspunkts beschreibt, den das Automatisierungselement darstellt.<br/> Dies sollte in Verbindung mit <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> <strong>aber LocalizedLandmarkType</strong> sollte immer Vorrang vor <strong>LandmarkType</strong> haben und verwendet werden, um das Landmark vor <strong>LandmarkType zu beschreiben.</strong><br/> Die Zeichenfolge muss mit der Benutzeroberflächensprache der Anwendung oder der Standardsprache der Benutzeroberfläche des Betriebssystems übereinstimmen.<br/> Variant-Typ: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td >Identifiziert die <strong>Name-Eigenschaft,</strong> bei der es sich um eine Zeichenfolge handelt, die den Namen des Automatisierungselements enthält.<br/> Die <strong>Name-Eigenschaft</strong> sollte mit dem Bezeichnungstext auf dem Bildschirm identisch sein. Der Name <strong>sollte z.</strong> &quot; B. Nach einem Schaltflächenelement mit der Bezeichnung &quot; Durchsuchen suchen &quot; &quot; sein. Die <strong>Name-Eigenschaft</strong> darf nicht das mnemonische Zeichen für die Zugriffsschlüssel (d. h. ) enthalten, das in der Textdarstellung &quot; & &quot; der Benutzeroberfläche unterstrichen ist. Außerdem sollte die <strong>Name-Eigenschaft</strong> keine erweiterte oder geänderte Version der Bezeichnung auf dem Bildschirm sein, da die Inkonsistenz zwischen Name und Bezeichnung zu Verwirrung zwischen Clientanwendungen und Benutzern führen kann.<br/> Wenn der entsprechende Bezeichnungstext auf dem Bildschirm nicht sichtbar ist oder durch Grafiken ersetzt wird, sollte alternativer Text ausgewählt werden. Der alternative Text sollte präzise, intuitiv und in der Benutzeroberflächensprache der Anwendung oder in der Standardsprache der Benutzeroberfläche des Betriebssystems lokalisiert sein. Der alternative Text sollte keine ausführliche Beschreibung der visuellen Details sein, sondern eine präzise Beschreibung der Benutzeroberflächenfunktion oder des Features, als wäre sie mit einfachem Text bezeichnet. Die Schaltfläche "Windows Startmenü" hat beispielsweise den Namen Start (Schaltfläche) statt Windows Logo auf blauen runden &quot; &quot; &quot; &quot; Kugelgrafiken (Schaltfläche). Weitere Informationen finden Sie unter <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">Erstellen von Textäquivalenten für Bilder.</a><br/> Wenn eine Benutzeroberflächenbezeichnung Textgrafiken verwendet (z. B. für eine Schaltfläche, die ein Element von links nach rechts hinzufügt), sollte die Name-Eigenschaft durch eine entsprechende Textalternative überschrieben werden (z. B. &quot; >> &quot; <strong></strong> &quot; &quot; Hinzufügen). Die Verwendung von Textgrafiken als Benutzeroberflächenbezeichnung wird jedoch aufgrund von Lokalisierungs- und Barrierefreiheitsbedenken nicht abgeraten.<br/> Die <strong>Name-Eigenschaft</strong> darf keine Informationen zur Steuerelementrolle oder zum Typ enthalten, z. B. Schaltfläche oder Liste. Andernfalls steht sie in Konflikt mit dem Text der &quot; &quot; &quot; &quot; <strong>LocalizedControlType-Eigenschaft,</strong> wenn diese beiden Eigenschaften angefügt werden (viele vorhandene Hilfstechnologien tun dies).<br/> Die <strong>Name-Eigenschaft</strong> kann nicht als eindeutiger Bezeichner für gleichgeordnete Elemente verwendet werden. Solange sie jedoch mit der Darstellung der Benutzeroberfläche konsistent ist, kann der gleiche <strong>Name-Wert</strong> von Peers unterstützt werden. Für die Testautomatisierung sollten die Clients die Verwendung der <strong>Eigenschaft AutomationId</strong> oder <strong>RuntimeId</strong> in Betracht ziehen.<br/> Textsteuerelemente müssen nicht immer die <strong>Name-Eigenschaft</strong> mit dem Text identisch sein, der im -Steuerelement angezeigt wird, solange das <strong>Textmuster</strong> ebenfalls unterstützt wird.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td >Identifiziert die <strong>NativeWindowHandle-Eigenschaft,</strong> bei der es sich um eine ganze Zahl handelt, die das Handle (<strong>HWND</strong>) des Automatisierungselementfensters darstellt, sofern vorhanden; Andernfalls ist diese Eigenschaft 0.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td >Identifiziert die <strong>OptimizeForVisualContent-Eigenschaft,</strong> bei der es sich um einen booleschen Wert handelt, der angibt, ob der Anbieter nur sichtbare Elemente verfügbar macht. Ein Anbieter kann diese Eigenschaft verwenden, um die Leistung bei der Arbeit mit sehr großen Inhaltsteilen zu optimieren. Wenn der Benutzer beispielsweise einen großen Teil des Inhalts durchgibt, kann der Anbieter Inhaltselemente zerstören, die nicht mehr sichtbar sind. Wenn ein Inhaltselement zerstört wird, sollte der Anbieter den <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> Fehlercode zurückgeben. Wird ab Windows 8 unterstützt.<br/> Variant-Typ: <strong>VT_BOOL</strong><br/> Standardwert: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td >Identifiziert die <strong>Orientation-Eigenschaft,</strong> die die Ausrichtung des steuerelements angibt, das durch das Automatisierungselement dargestellt wird. Die -Eigenschaft wird als Wert aus dem <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>Enumerationstyp OrientationType</strong></a> ausgedrückt.<br/> Die <strong>Orientation-Eigenschaft</strong> wird von Steuerelementen wie Bildlaufleisten und Schiebereglern unterstützt, die entweder eine vertikale oder eine horizontale Ausrichtung aufweisen können. Andernfalls kann es immer <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>sein, was bedeutet, dass das Steuerelement keine Ausrichtung hat.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td >Identifiziert die <strong>OutlineColor-Eigenschaft,</strong> die die Farbe angibt, die für die Kontur des Automatisierungselements verwendet wird. Dieses Attribut wird als <strong>COLORREF</strong>angegeben, ein 32-Bit-Wert, der zum Angeben einer RGB- oder RGBA-Farbe verwendet wird.<br/> Variantentyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td >Identifiziert die <strong>OutlineThickness-Eigenschaft,</strong> die die Breite für die Kontur des Automatisierungselements angibt.<br/> Variantentyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td >Identifiziert die <strong>PositionInSet-Eigenschaft,</strong> bei der es sich um eine 1-basierte ganze Zahl handelt, die einem Automatisierungselement zugeordnet ist. <strong>PositionInSet</strong> beschreibt die Ordnungsposition des Elements innerhalb einer Gruppe von Elementen, die als gleichgeordnete Elemente betrachtet werden.<br/> <strong>PositionInSet</strong> arbeitet in Koordination mit der <strong>SizeOfSet-Eigenschaft,</strong> um die Ordnungsposition in der Menge zu beschreiben.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td >Identifiziert die <strong>ProcessId-Eigenschaft,</strong> bei der es sich um eine ganze Zahl handelt, die den Prozessbezeichner (ID) des Automatisierungselements darstellt.<br/> Der Prozessbezeichner (ID) wird vom Betriebssystem zugewiesen. Sie wird in der <strong>PiD-Spalte</strong> der Registerkarte <strong>Prozesse</strong> in Task-Manager angezeigt.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td >Identifiziert die <strong>ProviderDescription-Eigenschaft,</strong> bei der es sich um eine formatierte Zeichenfolge handelt, die die Quellinformationen des Benutzeroberflächenautomatisierung Anbieters für das Automation-Element enthält, einschließlich Proxyinformationen.<br/> Variantentyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td >Identifiziert die <strong></strong> Rotationseigenschaft, die den Drehwinkel in nicht angegebenen Einheiten angibt.<br/> Variant-Typ: <strong>VT_R8</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td >Identifiziert die <strong>RuntimeId-Eigenschaft,</strong> bei der es sich um ein Array von ganzen Zahlen handelt, die den Bezeichner für ein Automatisierungselement darstellen.<br/> Der Bezeichner ist auf dem Desktop eindeutig, aber er ist garantiert nur innerhalb der Benutzeroberfläche des Desktops eindeutig, auf dem er generiert wurde. Bezeichner können im Laufe der Zeit wiederverwendet werden.<br/> Das Format von <strong>RuntimeId</strong> kann sich ändern. Der zurückgegebene Bezeichner sollte als nicht transparenter Wert behandelt und nur für Vergleiche verwendet werden. Beispielsweise, um zu bestimmen, ob sich ein Automatisierungselement im Cache befindet.<br/> Variantentyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td >Identifiziert die <strong>Size-Eigenschaft,</strong> die die Breite und Höhe des Automatisierungselements angibt.<br/> Variantentyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td >Identifiziert die <strong>SizeOfSet-Eigenschaft,</strong> bei der es sich um eine 1-basierte ganze Zahl handelt, die einem Automatisierungselement zugeordnet ist. <strong>SizeOfSet</strong> beschreibt die Anzahl der Automatisierungselemente in einer Gruppe oder Gruppe, die als gleichgeordnete Elemente betrachtet werden.<br/> <strong>SizeOfSet</strong> arbeitet in Koordination mit der <strong>PositionInSet-Eigenschaft,</strong> um die Anzahl der Elemente in der Menge zu beschreiben.<br/> Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td >Identifiziert die <strong>VisualEffects-Eigenschaft,</strong> bei der es sich um ein Bitfeld handelt, das Effekte auf das Automatisierungselement angibt, z. B. Schatten, Reflexion, Leuchteffekt, weiche Kanten oder Abschrägungen.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Variant-Typ: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows \[UWP-Apps für Server 2003-Desktop-Apps \|\]<br/>                                     |
| Header<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elementen](uiauto-propertiesforclients.md)
</dt> </dl>
