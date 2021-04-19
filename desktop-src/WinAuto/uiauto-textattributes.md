---
title: Benutzeroberflächenautomatisierungs-Text Attribute
description: In diesem Thema wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung die Format-und Stileigenschaften (Text Attribute) von Textinhalten verfügbar macht und eine Liste unterstützter Text Attribute bereitstellt.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- UI-Automatisierung, Text Attribute
- Text Attribute, Informationen zu
- Text Attribute, Variant-Typen
- Text Attribute, Datentypen
- Benutzeroberflächen Automatisierung, Liste der Attribute
- UI-Automatisierung, Liste von Textattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341536"
---
# <a name="ui-automation-text-attributes"></a>Benutzeroberflächenautomatisierungs-Text Attribute

In diesem Thema wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung die Format-und Stileigenschaften (*Text Attribute*) von Textinhalten verfügbar macht und eine Liste unterstützter Text Attribute bereitstellt.

Benutzeroberflächenautomatisierungs-Anbieter machen Text Attribute über die [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) -und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) -Methode des [TextRange](uiauto-about-text-and-textrange-patterns.md) -Steuerelement Musters verfügbar. Client Anwendungen verwenden die [**iuiautomationtextrange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) -Methode, um den Wert eines bestimmten Text Attributs für einen Textbereich abzurufen. Clients können die [**iuiautomationtextrange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) -Methode verwenden, um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Attribut verfügt. Wenn ein übereinstimmender Text gefunden wird, erstellt die-Methode einen neuen Textbereich, der den übereinstimmenden Text enthält.

Die Text Attribute in der folgenden Liste werden vom **TextRange** -Steuerelement Muster unterstützt. Die Attributnamen stammen aus den Benutzeroberflächenautomatisierungs-Text Attribut bezeichnerbezeichner. Das **AnimationStyle** -Attribut wird z. b. von Clients als [**UIA \_ animationstyleattributeid**](uiauto-textattribute-ids.md) (definiert in UIAutomationClient. h) und von Anbietern als **Text \_ AnimationStyle-Attribut- \_ \_ GUID** (definiert in uiautomationcoreapi. h) identifiziert. Weitere Informationen zu den einzelnen unterstützten Textattributen finden Sie unter [**Text Attribut**](uiauto-textattribute-ids.md)Bezeichner.

> [!Note]  
> Einige der aufgeführten Attribute werden ab Windows 8 unterstützt. Hinweise zur Versions Unterstützung finden Sie unter [**Text Attribut**](uiauto-textattribute-ids.md) Bezeichner.

 

Dieses Thema enthält folgende Abschnitte:

-   [Anmerkungsattribute](#annotation-attributes)
-   [Schriftartattribute](#font-attributes)
-   [Sprach Attribute](#language-attributes)
-   [Link-Attribut](#link-attribute)
-   [Seitenrand Attribute](#page-margin-attributes)
-   [Text Ausrichtungs Attribute](#text-alignment-attributes)
-   [Textfarbattribute](#text-color-attributes)
-   [Attribute für die Text Dekoration](#text-decoration-attributes)
-   [Textstilattribute](#text-style-attributes)
-   [Interaktions-und Auswahl Attribute](#interaction-and-selection-attributes)
-   [Zugehörige Themen](#related-topics)

## <a name="annotation-attributes"></a>Anmerkungsattribute

Anmerkung-Objekte und-Anmerkungen sind über die folgenden Attribute verfügbar.



| Attribut             | Bezeichner                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **Annotationobjects** | [**UIA \_ annotationobjecungsattributeid**](uiauto-textattribute-ids.md) |
| **Annotationtypes**   | [**UIA \_ annotationtypesattributeid**](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a>Schriftartattribute

Name, Größe und Gewichtung einer Schriftart sind über die folgenden Attribute verfügbar.



| Attribut      | Bezeichner                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ fontnameattributeid**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ fontsizeattributeid**](uiauto-textattribute-ids.md)     |
| **Schriftbreite** | [**UIA \_ fontweightattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Sprach Attribute

Informationen zur Sprache des Texts sind über die folgenden Attribute verfügbar.



| Attribut              | Bezeichner                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Kultur**            | [**UIA \_ cultureattributeid**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA- \_ textflowdirectionsattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Link-Attribut

Mit dem folgenden Attribut wird der Textbereich bereitstellt, der das Ziel eines Links in einem Dokument ist.



| Attribut | Bezeichner                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Link**  | [**UIA \_ linkattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Seitenrand Attribute

Die Begrenzungs Rechtecke eines Text Bereichs machen die Koordinaten des Texts auf der Seite nicht verfügbar. Ein Anbieter kann jedoch die Seitenrand Informationen mithilfe der folgenden Text Attribute verfügbar machen.



| Attribut          | Bezeichner                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ marginbottomattributeid**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ marginleadingattributeid**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ margintopattributeid**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ margintrailingattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Text Ausrichtungs Attribute

Informationen zur Textausrichtung, z. b. Einzug, Tabulator Einstellungen und horizontale Ausrichtung, sind über die folgenden Attribute verfügbar.



| Attribut                   | Bezeichner                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ horizontaltextalignmentattributeid**](uiauto-textattribute-ids.md) |
| **Indentationfirstline**    | [**UIA \_ indentationfirstlineattributeid**](uiauto-textattribute-ids.md)       |
| **Indentationleading**      | [**UIA \_ indentationleadingattributeid**](uiauto-textattribute-ids.md)           |
| **Indentationtrailing**     | [**UIA \_ indentationtrailingattributeid**](uiauto-textattribute-ids.md)         |
| **Registerkarten**                    | [**UIA \_ tabsattributeid**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Textfarbattribute

Die Vordergrund-und Hintergrund Textfarben sind über die folgenden Text Attribute verfügbar. Beide Farben werden als [**COLORREF**](/windows/desktop/gdi/colorref) -Datentyp angegeben.



| Attribut           | Bezeichner                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ backgroundcolorattributeid**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ foregroundcolorattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Attribute für die Text Dekoration

Text Dekorationen enthalten Bereiche wie z. b. Aufzählungs Zeichen, Unterstreichung und Animationen. Wenn Text führende Aufzählungen oder Ziffern enthält, sollte das Symbol oder der Text, der für die Aufzählungs Zeichen oder die Zahl verwendet wird, ggf. im Textstream enthalten sein.

Informationen zu Text Dekorationen sind über die folgenden Attribute verfügbar.



| Attribut              | Bezeichner                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ animationstyleattributeid**](uiauto-textattribute-ids.md)         |
| **Kugel Stil**        | [**UIA \_ -"bulletstyleattributeid"**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ outlinestylesattributeid**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ overlinecolorattributeid**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ overlinestyleattributeid**](uiauto-textattribute-ids.md)           |
| **StrikeThrough-Farbe** | [**UIA \_ StrikeThrough colorattributeid**](uiauto-textattribute-ids.md) |
| **StrikeThrough-Stil** | [**UIA \_ -Strip Item-Funktion**](uiauto-textattribute-ids.md) |
| **Unterlinecolor**     | [**UIA \_ underlinecolorattributeid**](uiauto-textattribute-ids.md)         |
| **Unterlinestyle**     | [**UIA \_ underlinestyleattributeid**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Textstilattribute

Informationen zu Textformaten sind auch über die folgenden Attribute verfügbar.



| Attribut         | Bezeichner                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ capstyleattributeid**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA- \_ ishiddenattributeid**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ isitali| tributeid**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ isumlyattributeid**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ issuperscriptattributeid**](uiauto-textattribute-ids.md) |
| **Isabonniert**   | [**UIA \_ isabonptattributeid**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Interaktions-und Auswahl Attribute

Informationen zur aktuellen Textauswahl im Bereich Bereich und Fokus sind über die folgenden Attribute verfügbar.



| Attribut              | Bezeichner                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ isactiveattributeid**](uiauto-textattribute-ids.md)           |
| **Selectionactiveend** | [**UIA \_ selectionactiveendattributeid**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ caretpositionattributeid**](uiauto-textattribute-ids.md)      |
| **Caretbidimode**      | [**UIA \_ caretbidimodeattributeid**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Informationen zu Benutzeroberflächenautomatisierungs-Text und TextRange-Steuerelement Mustern](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Text-und TextRange-Steuerelement Muster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 