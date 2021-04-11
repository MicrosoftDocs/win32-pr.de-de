---
title: Eigenschaften Bezeichner für Automatisierungselemente (UIAutomationClient. h)
description: In diesem Thema werden die benannten Konstanten beschrieben, mit denen die Eigenschaften von Microsoft UI Automation-Elementen identifiziert werden.
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
ms.openlocfilehash: 60c90b1a6d56fa62b6ddb241ce38c8cb2ae40afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105789"
---
# <a name="automation-element-property-identifiers"></a>Eigenschaften Bezeichner für Automatisierungselemente

In diesem Thema werden die benannten Konstanten beschrieben, mit denen die Eigenschaften von Microsoft UI Automation-Elementen identifiziert werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>AcceleratorKey</strong> -Eigenschaft, die eine Zeichenfolge mit den Tastenkombinationen (auch als Tastenkombinationen bezeichnet) für das Automation-Element enthält. <br/> Tastenkombinationen rufen eine Aktion auf. Beispielsweise wird "Strg + O" häufig verwendet, um das Dialogfeld "Datei öffnen" aufzurufen. Ein Automation-Element, das über die <strong>AcceleratorKey</strong> -Eigenschaft verfügt, kann das Start Steuerelement Muster für die Aktion implementieren <a href="uiauto-implementinginvoke.md">, die dem</a> shortcutbefehl entspricht.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>AccessKey</strong> -Eigenschaft, bei der es sich um eine Zeichenfolge mit dem Zugriffsschlüssel Zeichen für das Automation-Element handelt.<br/> Eine Zugriffstaste (manchmal auch als mnetmonisches bezeichnet) ist ein Zeichen im Text eines Menüs, Menü Elements oder einer Bezeichnung eines Steuer Elements, z. b. eine Schaltfläche, das die zugehörige Menüfunktion aktiviert. Wenn Sie z. b. das Menü Datei öffnen möchten, für das der Zugriffsschlüssel in der Regel F ist, drücken Sie den Benutzer ALT + F.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>annotationobjects</strong> -Eigenschaft, die eine Liste von Anmerkung-Objekten in einem Dokument ist, wie z. b. Comment, Header, Footer usw.<br/> Varianttyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>annotationtypes</strong> -Eigenschaft, die eine Liste der Typen von Anmerkungen in einem Dokument ist, wie z. b. Comment, Header, Footer usw.<br/> Varianttyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ariaproperties</strong> -Eigenschaft, die eine formatierte Zeichenfolge mit den Informationen zur verfügbaren Rich Internet Application (Aria)-Eigenschaft für das Automation-Element ist. Weitere Informationen zum Zuordnen von Aria-Zuständen und-Eigenschaften zu Eigenschaften und Funktionen der Benutzeroberflächen Automatisierung finden Sie unter <a href="uiauto-ariaspecification.md">UI Automation for W3C Accessible Rich Internet Applications Specification</a>.<br/> <strong>Ariaproperties</strong> ist eine Auflistung von Name-Wert-Paaren mit Trennzeichen von <strong>=</strong> (ist) und <strong>;</strong> (Semikolon), z &quot; . b. aktiviert = true; deaktiviert = false &quot; . Der <strong>\</strong> (umgekehrter Schrägstrich) wird als Escapezeichen verwendet, wenn diese Trennzeichen oder <strong>\</strong> in den Werten angezeigt werden. Aus Sicherheitsgründen und anderen Gründen kann die Anbieter Implementierung dieser Eigenschaft Schritte zum Überprüfen der ursprünglichen Aria-Eigenschaften ausführen. Es ist jedoch nicht erforderlich.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ariarole</strong> -Eigenschaft, die eine Zeichenfolge mit den Rollen Informationen für die barrierefreie Internet Anwendung (Rich Internet Application, Aria) für das Automation-Element ist. Weitere Informationen zum Mapping von Aria-Rollen zu Benutzeroberflächenautomatisierungs-Steuerelement Typen finden Sie unter <a href="uiauto-ariaspecification.md">UI Automation for W3C Accessible Rich Internet Applications Specification</a>.<br/>
<blockquote>
[!Note]<br />
Als Option kann der Benutzer-Agent auch eine lokalisierte Beschreibung der W3C-Aria-Rolle in der <strong>LocalizedControlType</strong> -Eigenschaft anbieten. Wenn die lokalisierte Zeichenfolge nicht angegeben wird, stellt das System die Standard Zeichenfolge <strong>LocalizedControlType</strong> für das Element bereit.
</blockquote>
<br/> <br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>AutomationId</strong> -Eigenschaft, die eine Zeichenfolge mit dem Benutzeroberflächenautomatisierungs-Bezeichner (ID) für das Automation-Element ist.<br/> Wenn Sie verfügbar ist, muss die <strong>AutomationId</strong> eines Elements in jeder Instanz der Anwendung identisch sein, unabhängig von der lokalen Sprache. Der Wert sollte bei gleich geordneten Elementen eindeutig sein, ist aber nicht unbedingt auf dem gesamten Desktop eindeutig. Beispielsweise können mehrere Instanzen einer Anwendung oder mehrere Ordner Sichten in Microsoft Windows Explorer Elemente mit der gleichen <strong>AutomationId</strong> -Eigenschaft enthalten, wie z &quot; . b. systemmenubar &quot; .<br/> Obwohl die Unterstützung für <strong>AutomationId</strong> immer für eine bessere Unterstützung automatisierter Tests empfohlen wird, ist diese Eigenschaft nicht obligatorisch. Wenn es unterstützt wird, ist <strong>AutomationId</strong> nützlich für das Erstellen eines Test Automatisierungs Skripts, das unabhängig von der Benutzeroberflächen Sprache ausgeführt wird. Clients sollten keine Annahmen bezüglich der von anderen Anwendungen verfügbar gemachten <strong>AutomationId</strong> -Werte treffen. " <strong>AutomationId</strong> " ist nicht garantiert, dass Sie über verschiedene Releases oder Builds einer Anwendung hinweg stabil ist.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>boundingrechteck</strong> -Eigenschaft, die die Koordinaten des Rechtecks angibt, das das Automatisierungs Element vollständig einschließt. Das Rechteck wird in physischen Bildschirm Koordinaten ausgedrückt. Sie kann Punkte enthalten, die nicht klickbar sind, wenn die Form oder der klickbare Bereich des Benutzeroberflächen Elements unregelmäßig ist, oder wenn das Element von anderen Benutzeroberflächen Elementen verdeckt wird.<br/> Varianttyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: [0, 0, 0, 0]<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft ist <strong>null</strong> , wenn das Element zurzeit keine Benutzeroberfläche anzeigt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>CenterPoint</strong> -Eigenschaft, die die Mittelpunkt-X-und Y-Koordinaten des Automation-Elements angibt. Der Koordinaten Bereich ist das, was der Anbieter logisch als Seite ansieht.<br/> Varianttyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>className</strong> -Eigenschaft, bei der es sich um eine Zeichenfolge mit dem Klassennamen für das Automation-Element handelt, das vom Steuerelement Entwickler zugewiesen wird.<br/> Der Klassenname hängt von der Implementierung des Benutzeroberflächenautomatisierungs-Anbieters ab und ist daher nicht immer in einem Standardformat. Wenn der Klassenname jedoch bekannt ist, kann er verwendet werden, um zu überprüfen, ob eine Anwendung mit dem erwarteten Automation-Element arbeitet.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>clickablepoint</strong> -Eigenschaft, bei der es sich um einen Punkt auf dem Automation-Element handelt, auf das geklickt werden kann. Auf ein Element kann nicht geklickt werden, wenn es vollständig oder teilweise von einem anderen Fenster verdeckt wird.<br/> Varianttyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td style="text-align: left;">Identifiziert die <strong>controllerfor</strong> -Eigenschaft, die ein Array von Automatisierungs Elementen ist, die von dem Automation-Element bearbeitet werden, das diese Eigenschaft unterstützt.<br/> <strong>Controllerfor</strong> wird verwendet, wenn sich ein Automation-Element auf ein oder mehrere Segmente der Anwendungs Benutzeroberfläche oder des Desktops auswirkt. Andernfalls ist es schwierig, die Auswirkung des Steuerungs Vorgangs auf Benutzeroberflächen Elemente zuzuordnen.<br/> Dieser Bezeichner wird häufig für die Barrierefreiheit empfohlen, die <a href="/windows/uwp/design/accessibility/accessible-text-requirements">automatisch vorgeschlagen</a>wird.<br/> Varianttyp für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Varianttyp für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>iuiautomationelementarray</strong></a> )<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ControlType</strong> -Eigenschaft, die eine Klasse ist, die den Typ des Automatisierungs Elements identifiziert. <strong>ControlType</strong> definiert Merkmale der Benutzeroberflächen Elemente durch bekannte Benutzeroberflächen-Steuerelement primitive, z. b. Schaltflächen oder Kontrollkästchen. <br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Verwenden Sie den Standardwert nur, wenn das Automation-Element einen völlig neuen Typ von Steuerelement darstellt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>Culture</strong> -Eigenschaft, die einen Gebiets Schema Bezeichner für das Automation-Element enthält (z. b <code>0x0409</code> &quot; . für en-US &quot; oder Englisch (USA)).<br/> Jedes Gebiets Schema hat einen eindeutigen Bezeichner, einen 32-Bit-Wert, der aus einer Sprach-ID und einer Sortierreihenfolge-ID besteht. Der Gebiets Schema Bezeichner ist eine standardmäßige internationale numerische Abkürzung und verfügt über die Komponenten, die zur eindeutigen Identifizierung eines der installierten, Betriebssystem definierten Gebiets Schemas erforderlich sind. Weitere Informationen finden Sie unter <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">sprach Bezeichner-Konstanten und-</a>Zeichen folgen.<br/> Diese Eigenschaft ist möglicherweise auf der Grundlage der einzelnen Steuerelemente vorhanden, ist jedoch in der Regel nur auf Anwendungsebene verfügbar.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>DescribedBy</strong> -Eigenschaft, die ein Array von-Elementen ist, die weitere Informationen über das Automation-Element bereitstellen.<br/> <strong>DescribedBy</strong> wird verwendet, wenn ein Automation-Element von einem anderen Segment der Anwendungs Benutzeroberfläche erläutert wird. Beispielsweise kann die-Eigenschaft auf ein Textelement von &quot; 2.529 Elementen in 85 Gruppen verweisen, 10 Elemente, die &quot; aus einem komplexen benutzerdefinierten Listen Objekt ausgewählt wurden. Anstatt das Objektmodell für Clients zum Digest ähnlicher Informationen zu verwenden, kann die <strong>DescribedBy</strong> -Eigenschaft schnellen Zugriff auf das UI-Element bieten, das möglicherweise bereits nützliche Endbenutzer Informationen bereitstellt, die das UI-Element beschreiben.<br/> Varianttyp für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Varianttyp für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>iuiautomationelementarray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>FillColor</strong> -Eigenschaft, die die Farbe angibt, die zum Ausfüllen des Automatisierungs Elements verwendet wird. Dieses Attribut wird als COLORREF angegeben, einem 32-Bit-Wert, der zum Angeben der RGB-oder RGBA-Farbe verwendet wird.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>FillType</strong> -Eigenschaft, die das Muster angibt, das zum Ausfüllen des Automatisierungs Elements verwendet wird, z. b. keine, Farbe, Farbverlauf, Bild, Muster usw.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td style="text-align: left;">Gibt die <strong>flowsfrom</strong> -Eigenschaft an, bei der es sich um ein Array von Automatisierungs Elementen handelt, das die Lesefolge vor dem aktuellen Automation-Element vorschlägt. Unterstützt ab Windows 8.<br/> Die <strong>flowsfrom</strong> -Eigenschaft gibt die Lesereihenfolge an, wenn Automatisierungselemente nicht in der gleichen Lesefolge wie vom Benutzer erkannt oder strukturiert werden. Obwohl die <strong>flowsfrom</strong> -Eigenschaft mehrere vorangehende Elemente angeben kann, enthält Sie in der Regel nur das vorherige Element in der Lesereihenfolge.<br/> Varianttyp für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Varianttyp für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>iuiautomationelementarray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>flowsto</strong> -Eigenschaft, die ein Array von Automatisierungs Elementen ist, das die Lesefolge nach dem aktuellen Automation-Element vorschlägt.<br/> Die <strong>flowsto</strong> -Eigenschaft gibt die Lesereihenfolge an, wenn Automatisierungselemente nicht in der gleichen Lesefolge wie vom Benutzer erkannt oder strukturiert werden. Obwohl die <strong>flowsto</strong> -Eigenschaft mehrere nachfolgende Elemente angeben kann, enthält Sie in der Regel nur das nächste Element in der Lesereihenfolge.<br/> Varianttyp für Anbieter: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Varianttyp für Clients: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>iuiautomationelementarray</strong></a>)<br/> Standardwert: leeres Array<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>frameworkid</strong> -Eigenschaft, die eine Zeichenfolge mit dem Namen des zugrunde liegenden Benutzeroberflächen-Frameworks ist, zu dem das Automation-Element gehört.<br/> Mit der <strong>frameworkid</strong> können Client Anwendungen Automatisierungselemente abhängig vom jeweiligen Benutzeroberflächen Framework unterschiedlich verarbeiten. Beispiele für Eigenschaftswerte sind &quot; Win32 &quot; , &quot; WinForm &quot; und &quot; directui &quot; .<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td style="text-align: left;">Die <strong>fulldescription</strong> -Eigenschaft macht eine lokalisierte Zeichenfolge verfügbar, die erweiterten Beschreibungstext für ein Element enthalten kann. <strong>Fulldescription</strong> kann eine vollständigere Beschreibung eines Elements enthalten, als für den Element <strong>Namen</strong>geeignet ist.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>HasKeyboardFocus</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungs Element über den Tastaturfokus verfügt.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>headinglevel</strong> -Eigenschaft, die die Überschrift Ebene eines Benutzeroberflächenautomatisierungs-Elements angibt.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>HelpText</strong> -Eigenschaft, die eine Hilfe Text Zeichenfolge ist, die dem Automation-Element zugeordnet ist.<br/> Die <strong>HelpText</strong> -Eigenschaft kann mit Platzhalter Text unterstützt werden, der in Bearbeitungs-oder Listen Steuerelementen angezeigt wird. Beispiel: &quot; Text hier eingeben für Search &quot; ist ein guter Kandidat für die <strong>HelpText</strong> -Eigenschaft für ein Bearbeitungs Steuerelement, das den Text vor der tatsächlichen Eingabe des Benutzers platziert. Die Name-Eigenschaft des Bearbeitungs Steuer Elements ist jedoch nicht ausreichend.<br/> Wenn <strong>HelpText</strong> unterstützt wird, muss die Zeichenfolge der Benutzeroberflächen Sprache der Anwendung oder der Standardbenutzer Oberfläche des Betriebssystems entsprechen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>IsContentElement</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Element in der Inhaltsansicht der Automatisierungs Elementstruktur angezeigt wird. Weitere Informationen finden Sie unter <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/>
<blockquote>
[!Note]<br />
Damit ein Element in der Inhaltsansicht angezeigt wird, müssen sowohl die <strong>IsContentElement</strong> -Eigenschaft als auch die <strong>IsControlElement</strong> -Eigenschaft den Wert " <strong>true</strong>" aufweisen.
</blockquote>
<br/> <br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>true</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>IsControlElement</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Element in der Steuerelement Ansicht der Automatisierungs Elementstruktur angezeigt wird. Weitere Informationen finden Sie unter <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>true</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>isdatavalidforform</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob der eingegebene oder ausgewählte Wert für die dem Automation-Element zugeordnete Formular Regel gültig ist. Wenn der Benutzer z. b. &quot; 425-555-5555 &quot; für ein ZIP-Codefeld eingegeben hat, das 5 oder 9 Ziffern erfordert, kann die <strong>isdatavalidforform</strong> -Eigenschaft auf <strong>false</strong> festgelegt werden, um anzugeben, dass die Daten ungültig sind.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>

<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>isdialog</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungs Element ein Dialogfenster ist. Hilfstechnologien wie Sprachausgaben sprechen z. b. in der Regel den Titel des Dialog Felds, das Steuerelement mit dem Fokus im Dialogfeld und den Inhalt des Dialog Felds bis zum Steuerelement mit Fokus (möchten &quot; Sie die Änderungen vor dem Schließen speichern &quot; ). Bei Standard Fenstern spricht eine Sprachausgabe in der Regel den Fenstertitel, gefolgt vom Steuerelement mit Fokus. Die <strong>isdialog</strong> -Eigenschaft kann auf <strong>true</strong> festgelegt werden, um anzugeben, dass die Client Anwendung das-Element als Dialogfenster behandeln soll.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>

<tr class="even">
<td style="text-align: left;"><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>isaktivierte</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das vom Automation-Element referenzierte Benutzeroberflächen Element aktiviert ist und mit interagiert werden kann.<br/> Wenn der aktivierte Zustand eines Steuer Elements <strong>false</strong>ist, wird davon ausgegangen, dass untergeordnete Steuerelemente ebenfalls nicht aktiviert sind. Clients sollten keine Eigenschaften geänderten Ereignisse von untergeordneten Elementen erwarten, wenn sich der Status des übergeordneten Steuer Elements ändert.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>iskeyboardfocverwendbare</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungs Element den Tastaturfokus annehmen kann.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>IsOffscreen</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungs Element vollständig von der Ansicht (z. b. einem Element in einem Listenfeld außerhalb des Viewports des Container Objekts) oder von der Ansicht (z. b. einem Element in einer Strukturansicht oder einem minimierten Fenster) entfernt wurde. Wenn das Element über einen durch Klicken aktivierbaren Punkt verfügt, der den Fokus erhalten kann, wird das Element als Bildschirm Bild angezeigt, während ein Teil des Elements außerhalb des Bildschirms ist.<br/> Der Wert der-Eigenschaft ist nicht von der Okklusion durch andere Fenster oder davon abhängig, ob das Element auf einem bestimmten Monitor sichtbar ist.<br/> Wenn die <strong>IsOffscreen</strong> -Eigenschaft auf <strong>true</strong>gesetzt ist, wird das Benutzeroberflächen Element per Bildlauf außerhalb des Bildschirms oder reduziert. Das Element ist vorübergehend ausgeblendet, verbleibt aber in der Wahrnehmung des Endbenutzers und wird weiterhin im Benutzeroberflächen Modell enthalten sein. Das Objekt kann wieder angezeigt werden, indem Sie einen Bildlauf durchführen, auf eine Dropdown-Dropdown-Ansicht klicken usw.<br/> Objekte, die der Endbenutzer überhaupt nicht wahrnimmt oder die Programm gesteuert ausgeblendet sind &quot; (z. b. &quot; ein Dialogfeld, das verworfen wurde, aber das zugrunde liegende Objekt wird immer noch von der Anwendung zwischengespeichert), sollte sich nicht in der Automatisierungs Elementstruktur an erster Stelle befinden (anstatt den Status von <strong>IsOffscreen</strong> auf <strong>true</strong>festzulegen).<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>IsPassword</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automation-Element geschützten Inhalt oder ein Kennwort enthält.<br/> Wenn die <strong>IsPassword</strong> -Eigenschaft auf <strong>true</strong> festgelegt ist und das Element über den Tastaturfokus verfügt, sollte eine Client Anwendung die Tastatur Rückgabe oder das Feedback der Tastatureingabe deaktivieren, die die geschützten Informationen des Benutzers verfügbar machen kann. Wenn Sie versuchen, auf die <strong>value</strong> -Eigenschaft des geschützten Elements (Bearbeitungs Steuerelement) zuzugreifen, tritt möglicherweise ein Fehler auf.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>isperipheral</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automatisierungs Element eine Peripherie Benutzeroberfläche darstellt. Die Benutzeroberfläche für Peripheriegeräte wird angezeigt und unterstützt Benutzerinteraktionen, aber der Tastaturfokus wird nicht angezeigt. Beispiele für die Benutzeroberfläche für Peripheriegeräte sind Popups, Flyouts, Kontextmenüs oder Gleit Komma Benachrichtigungen. Unterstützt ab Windows 8.1.<br/> Wenn die <strong>isperipheral</strong> -Eigenschaft den Wert <strong>true</strong>hat, kann eine Client Anwendung nicht davon ausgehen, dass der Fokus vom Element übernommen wurde, auch wenn Sie derzeit Tastatur interaktiv ist.<br/> Diese Eigenschaft ist für diese Steuerelement Typen relevant:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>isrequirements dforform</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob das Automation-Element auf einem Formular ausgefüllt werden muss.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ItemStatus</strong> -Eigenschaft, bei der es sich um eine Text Zeichenfolge handelt, die den Status eines Elements des Automation-Elements beschreibt.<br/> <strong>ItemStatus</strong> ermöglicht einem Client, festzustellen, ob ein Element Statusinformationen zu einem Element übermittelt und wie der Status lautet. Beispielsweise kann ein Element, das einem Kontakt in einer Messaging Anwendung zugeordnet ist, &quot; ausgelastet &quot; oder verbunden sein &quot; &quot; .<br/> Wenn <strong>ItemStatus</strong> unterstützt wird, muss die Zeichenfolge mit der Benutzeroberflächen Sprache der Anwendung oder der Standardbenutzer Oberfläche des Betriebssystems übereinstimmen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ItemType</strong> -Eigenschaft, bei der es sich um eine Text Zeichenfolge handelt, die den Typ des Automatisierungs Elements beschreibt.<br/> <strong>ItemType</strong> dient zum Abrufen von Informationen zu Elementen in einer Liste, Strukturansicht oder einem Datenraster. Ein Element in einer Datei Verzeichnis Ansicht kann z. b. eine &quot; Dokument Datei &quot; oder ein &quot; Ordner sein &quot; .<br/> Wenn <strong>ItemType</strong> unterstützt wird, muss die Zeichenfolge mit der Benutzeroberflächen Sprache der Anwendung oder der Standardbenutzer Oberfläche des Betriebssystems übereinstimmen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die Eigenschaft " <strong>LabeledBy</strong> ", bei der es sich um ein Automation-Element handelt, das die Text Bezeichnung für dieses Element enthält.<br/> Diese Eigenschaft kann verwendet werden, um z. b. die statische Text Bezeichnung für ein Kombinations Feld abzurufen.<br/> Varianttyp: <strong>VT_UNKNOWN</strong><br/> Standardwert: <strong>null</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die Eigenschaft " <strong>landmarktype</strong> ", bei der es sich um einen einem Element zugeordneten <a href="landmark-type-identifiers.md"><strong>Bezeichner für einen Bezeichner</strong></a><br/> Die Eigenschaft " <strong>landmarktype</strong> " beschreibt ein Element, das eine Gruppe von Elementen darstellt. Beispielsweise kann ein Such-Landmark einen Satz verknüpfter Steuerelemente für die Suche darstellen.<br/> Wenn <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> verwendet wird, ist <strong>UIA_LocalizedLandmarkTypePropertyId</strong> erforderlich, um das benutzerdefinierte Wahrzeichen zu beschreiben.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>Level</strong> -Eigenschaft, die eine 1-basierte Ganzzahl ist, die einem Automation-Element zugeordnet ist.<br/> Die <strong>Level</strong> -Eigenschaft beschreibt den Speicherort eines Elements innerhalb einer hierarchischen oder unterbrochenen hierarchischen Struktur. Beispielsweise können eine aufzählige/nummerierte Liste, Überschriften oder andere strukturierte Datenelemente über verschiedene Beziehungen zwischen übergeordneten und untergeordneten Elementen verfügen. <strong>Ebene</strong> beschreibt, wo sich das Element in der Struktur befindet.<br/> Es wird empfohlen, das <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">customnavigation-Steuerelement Muster</a> zusammen mit der- <strong>Ebene</strong>zu verwenden.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>liveseding</strong> -Eigenschaft, die von einem Automation-Element unterstützt wird, das einen Live Bereich darstellt. Die <strong>livesetts</strong> -Eigenschaft gibt den richtentyp &quot; &quot; an, der von einem Client verwendet werden soll, um den Benutzer über Änderungen am Live Bereich zu benachrichtigen. Bei dieser Eigenschaft kann es sich um einen der Werte aus der <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>livesetts</strong></a> -Enumeration handeln. Unterstützt ab Windows 8.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>LocalizedControlType</strong> -Eigenschaft, die eine Text Zeichenfolge ist, die den Typ des Steuer Elements beschreibt, das das Automation-Element darstellt. Die Zeichenfolge sollte nur Kleinbuchstaben enthalten:
<ul>
<li>Korrigieren: &quot; Schaltfläche&quot;</li>
<li>Falsch: &quot; Schaltfläche&quot;</li>
</ul>
<br/> Wenn <strong>LocalizedControlType</strong> vom Element Anbieter nicht angegeben wird, wird die standardmäßige lokalisierte Zeichenfolge vom Framework gemäß dem Steuer Elementtyp des Elements (z. b. &quot; Schaltfläche &quot; für den Steuer Elementtyp " <a href="uiauto-supportbuttoncontroltype.md">Button</a> ") bereitgestellt. Ein Automatisierungs Element mit dem <strong>benutzerdefinierten</strong> Steuer Elementtyp muss eine lokalisierte Steuer Elementtyp Zeichenfolge unterstützen, die die Rolle des Elements darstellt (z. b. &quot; Farb &quot; Auswahl für ein benutzerdefiniertes Steuerelement, mit dem Benutzer Farben auswählen und angeben können).<br/> Wenn ein benutzerdefinierter Wert angegeben wird, muss die Zeichenfolge der Benutzeroberflächen Sprache der Anwendung oder der Standardbenutzer Oberfläche des Betriebssystems entsprechen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td style="text-align: left;">Identifiziert den <strong>localizedlandmarktype</strong>, bei dem es sich um eine Text Zeichenfolge handelt, die den Typ des vom Automation-Element dargestellten durch Zeichens beschreibt.<br/> Dies sollte zusammen mit den <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> verwendet werden. Allerdings sollte <strong>localizedlandmarktype</strong> immer Vorrang vor " <strong>landmarktype</strong> " haben und vor " <strong>landmarktype</strong>" verwendet werden, um das Landmark zu beschreiben.<br/> Die Zeichenfolge muss der Benutzeroberflächen Sprache der Anwendung oder der Standardbenutzer Oberfläche des Betriebssystems entsprechen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>Name</strong> -Eigenschaft, bei der es sich um eine Zeichenfolge handelt, die den Namen des Automation-Elements enthält.<br/> Die <strong>Name</strong> -Eigenschaft sollte mit dem Bezeichnungs Text auf dem Bildschirm identisch sein. Beispielsweise sollte <strong>Name</strong> durchsuchen &quot; &quot; nach einem Button-Element mit der Bezeichnung &quot; Durchsuchen gesucht werden &quot; . Die <strong>Name</strong> -Eigenschaft darf kein mnetmonisches Zeichen für die Zugriffsschlüssel enthalten (d. h &quot; & &quot; .), das in der UI-Textpräsentation unterstrichen ist. Außerdem sollte die <strong>Name</strong> -Eigenschaft keine erweiterte oder geänderte Version der Bildschirm Bezeichnung sein, da die Inkonsistenz zwischen dem Namen und der Bezeichnung bei Client Anwendungen und Benutzern Verwirrung verursachen kann.<br/> Wenn der entsprechende Bezeichnungs Text auf dem Bildschirm nicht sichtbar ist oder durch Grafiken ersetzt wird, sollte alternativer Text ausgewählt werden. Der Alternative Text sollte präzise, intuitiv und in der Benutzeroberflächen Sprache der Anwendung oder in der Standardbenutzer Oberfläche des Betriebssystems lokalisiert werden. Der Alternative Text sollte keine ausführliche Beschreibung der visuellen Details, sondern eine präzise Beschreibung der UI-Funktion oder-Funktion sein, als ob Sie durch einfachen Text gekennzeichnet wäre. Beispielsweise wird die Windows-Menü Schaltfläche &quot; Start &quot; (Schaltfläche) anstelle von &quot; Windows-Logo auf der blauen runden Kugel Grafik &quot; (Schaltfläche) benannt. Weitere Informationen finden Sie unter <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">Erstellen von Text Entsprechungen für Bilder</a>.<br/> Wenn eine Benutzeroberflächen Bezeichnung Text Grafiken verwendet (z. b. mit &quot; >> &quot; für eine Schaltfläche, die ein Element von links nach rechts hinzufügt), sollte die <strong>Name</strong> -Eigenschaft durch eine entsprechende Text Alternative (z &quot; . b. Add) überschrieben werden &quot; . Die Vorgehensweise bei der Verwendung von Text Grafiken als Benutzeroberflächen Bezeichnung wird jedoch aufgrund von Lokalisierungs-und Barrierefreiheits Problemen nicht empfohlen.<br/> Die <strong>Name</strong> -Eigenschaft darf keine Steuerelement-oder Typinformationen &quot; (z. b &quot; . Schaltfläche oder &quot; Liste) enthalten &quot; . andernfalls steht Sie in Konflikt mit dem Text aus der <strong>LocalizedControlType</strong> -Eigenschaft, wenn diese beiden Eigenschaften angefügt werden (viele vorhandene Hilfstechnologien bewirken dies).<br/> Die <strong>Name</strong> -Eigenschaft kann nicht als eindeutiger Bezeichner untergeordneten Elementen verwendet werden. Solange Sie jedoch mit der Darstellung der Benutzeroberfläche konsistent ist, kann der gleiche <strong>namens</strong> Wert von Peers unterstützt werden. Für die Testautomatisierung sollten die Clients die Verwendung der <strong>AutomationId</strong> -Eigenschaft oder der <strong>runtimeId-</strong> Eigenschaft in Erwägung gezogen werden.<br/> Bei Text Steuerelementen muss die <strong>Name</strong> -Eigenschaft nicht immer identisch mit dem Text sein, der im Steuerelement angezeigt wird, solange das <strong>Text</strong> Muster ebenfalls unterstützt wird.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>nativewindowhandle</strong> -Eigenschaft, bei der es sich um eine ganze Zahl handelt, die das Handle (<strong>HWND</strong>) des Automatisierungs Element Fensters darstellt (sofern vorhanden). Andernfalls ist diese Eigenschaft 0 (null).<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>optimizeforvisualcontent</strong> -Eigenschaft, bei der es sich um einen booleschen Wert handelt, der angibt, ob der Anbieter nur sichtbare Elemente verfügbar macht. Ein Anbieter kann diese Eigenschaft verwenden, um die Leistung bei der Arbeit mit sehr großen Inhalts Elementen zu optimieren. Wenn der Benutzer z. b. einen großen Teil des Inhalts durchläuft, kann der Anbieter Inhaltselemente zerstören, die nicht mehr sichtbar sind. Wenn ein Inhalts Element zerstört wird, sollte der Anbieter den <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> -Fehlercode zurückgeben. Unterstützt ab Windows 8.<br/> Varianttyp: <strong>VT_BOOL</strong><br/> Standardwert: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>Orientation</strong> -Eigenschaft, die die Ausrichtung des Steuer Elements angibt, das vom Automation-Element dargestellt wird. Die-Eigenschaft wird als Wert aus dem enumerierten Typ " <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType</strong></a> " ausgedrückt.<br/> Die <strong>Orientation</strong> -Eigenschaft wird von Steuerelementen wie Bild Lauf leisten und Schieberegler unterstützt, die entweder eine vertikale oder eine horizontale Ausrichtung aufweisen können. Andernfalls kann Sie immer <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>werden, was bedeutet, dass das Steuerelement keine Ausrichtung hat.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>OutlineColor</strong> -Eigenschaft, die die Farbe angibt, die für die Gliederung des Automation-Elements verwendet wird. Dieses Attribut wird als <strong>COLORREF</strong>angegeben, einem 32-Bit-Wert, der zum Angeben der RGB-oder RGBA-Farbe verwendet wird.<br/> Varianttyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>outlinethickness</strong> -Eigenschaft, die die Breite für die Gliederung des Automation-Elements angibt.<br/> Varianttyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>positioninset</strong> -Eigenschaft, bei der es sich um eine 1-basierte Ganzzahl handelt, die einem Automatisierungs Element zugeordnet ist. <strong>Positioninset</strong> beschreibt die Ordinalposition des Elements innerhalb einer Menge von Elementen, die als gleich geordnete Elemente betrachtet werden.<br/> <strong>Positioninset</strong> arbeitet mit der <strong>sizeofset</strong> -Eigenschaft zusammen, um den ordinalspeicherort im Satz zu beschreiben.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ProcessID-</strong> Eigenschaft, bei der es sich um eine ganze Zahl handelt, die den Prozess Bezeichner (ID) des Automation-Elements darstellt.<br/> Der Prozess Bezeichner (ID) wird vom Betriebssystem zugewiesen. Es ist in der Spalte <strong>PID</strong> der Registerkarte <strong>Prozesse</strong> im Task-Manager zu sehen.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>ProviderDescription</strong> -Eigenschaft, die eine formatierte Zeichenfolge ist, die die Quell Informationen des Benutzeroberflächenautomatisierungs-Anbieters für das Automation-Element enthält, einschließlich der Proxy Informationen.<br/> Varianttyp: <strong>VT_BSTR</strong><br/> Standardwert: leere Zeichenfolge<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>Rotations</strong> Eigenschaft, die den Drehwinkel in nicht angegebenen Einheiten angibt.<br/> Varianttyp: <strong>VT_R8</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>runtimeId-</strong> Eigenschaft, bei der es sich um ein Array von ganzen Zahlen handelt, das den Bezeichner für ein Automatisierungs Element darstellt.<br/> Der Bezeichner ist auf dem Desktop eindeutig, aber es ist sichergestellt, dass er nur innerhalb der Benutzeroberfläche des Desktops eindeutig ist, auf dem er generiert wurde. Bezeichner können im Laufe der Zeit wieder verwendet werden.<br/> Das Format von <strong>runtimeId</strong> kann sich ändern. Der zurückgegebene Bezeichner sollte als nicht transparenter Wert behandelt und nur für den Vergleich verwendet werden. beispielsweise, um zu bestimmen, ob sich ein Automation-Element im Cache befindet.<br/> Varianttyp: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>size</strong> -Eigenschaft, die die Breite und Höhe des Automation-Elements angibt.<br/> Varianttyp: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Standardwert: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>sizeofset</strong> -Eigenschaft, bei der es sich um eine 1-basierte Ganzzahl handelt, die einem Automatisierungs Element zugeordnet ist. <strong>Sizeofset</strong> beschreibt die Anzahl der Automatisierungselemente in einer Gruppe oder einer Gruppe, die als gleich geordnete Elemente angesehen werden.<br/> <strong>Sizeofset</strong> arbeitet in Abstimmung mit der <strong>positioninset</strong> -Eigenschaft, um die Anzahl der Elemente in der Menge zu beschreiben.<br/> Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td style="text-align: left;">Bezeichnet die <strong>visualeffects</strong> -Eigenschaft, bei der es sich um ein Bitfeld handelt, das Auswirkungen auf das Automatisierungs Element angibt, z. b. Schatten, Reflektion, Glanz, weiche Kanten oder Abschrägung.<br/> Visualeffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Varianttyp: <strong>VT_I4</strong><br/> Standardwert: 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[UWP-Apps für Windows XP-Desktop-Apps \|\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md)
</dt> </dl>
