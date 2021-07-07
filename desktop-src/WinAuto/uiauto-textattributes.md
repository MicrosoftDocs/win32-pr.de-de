---
title: Benutzeroberflächenautomatisierung Textattribute
description: In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung die Format- und Stileigenschaften (Textattribute) von Textinhalten verfügbar macht und eine Liste der unterstützten Textattribute enthält.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Benutzeroberflächenautomatisierung,Textattribute
- Textattribute,About
- Textattribute,Variant-Typen
- Textattribute,Datentypen
- Benutzeroberflächenautomatisierung,Liste der Attribute
- Benutzeroberflächenautomatisierung,Liste der Textattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353623"
---
# <a name="ui-automation-text-attributes"></a>Benutzeroberflächenautomatisierung Textattribute

In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung die Format- und Formateigenschaften *(* Textattribute ) von Textinhalten verfügbar macht und eine Liste der unterstützten Textattribute enthält.

Benutzeroberflächenautomatisierung anbieter machen Textattribute über die [**Methoden GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) und [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) des [TextRange-Steuerelementmusters](uiauto-about-text-and-textrange-patterns.md) verfügbar. Clientanwendungen verwenden die [**IUIAutomationTextRange::GetAttributeValue-Methode,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) um den Wert eines bestimmten Textattributs für einen Textbereich abzurufen. Clients können die [**IUIAutomationTextRange::FindAttribute-Methode verwenden,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) um einen Textbereich nach Text zu durchsuchen, der über ein bestimmtes Attribut verfügt. Wenn übereinstimmenden Text gefunden wird, erstellt die Methode einen neuen Textbereich, der den übereinstimmenden Text enthält.

Die Textattribute in der folgenden Liste werden vom **TextRange-Steuerelementmuster** unterstützt. Die Attributnamen werden von den Benutzeroberflächenautomatisierung Textattributbezeichnern abgeleitet. Das **AnimationStyle-Attribut** wird beispielsweise von Clients als [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definiert in Uiautomationclient.h) und von Anbietern als **Text \_ AnimationStyle \_ Attribute \_ GUID** (definiert in Uiautomationcoreapi.h) identifiziert. Weitere Informationen zu jedem unterstützten Textattribut finden Sie unter [**Textattributbezeichner**](uiauto-textattribute-ids.md).

> [!Note]  
> Einige der aufgeführten Attribute werden ab Windows 8. Hinweise [**zur Versionsunterstützung finden**](uiauto-textattribute-ids.md) Sie unter Textattributbezeichner.

 

Dieses Thema enthält folgende Abschnitte:

-   [Anmerkungsattribute](#annotation-attributes)
-   [Schriftartattribute](#font-attributes)
-   [Sprachattribute](#language-attributes)
-   [Linkattribut](#link-attribute)
-   [Seitenrandattribute](#page-margin-attributes)
-   [Textausrichtungsattribute](#text-alignment-attributes)
-   [Textfarbattribute](#text-color-attributes)
-   [Textdekorationsattribute](#text-decoration-attributes)
-   [Textformatattribute](#text-style-attributes)
-   [Interaktions- und Auswahlattribute](#interaction-and-selection-attributes)
-   [Verwandte Themen](#related-topics)

## <a name="annotation-attributes"></a>Anmerkungsattribute

Anmerkungsobjekte und Anmerkungstypen sind über die folgenden Attribute verfügbar.



| attribute             | Bezeichner                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-annotation-type-identifiers.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a>Schriftartattribute

Der Name, die Größe und die Gewichtung einer Schriftart sind über die folgenden Attribute verfügbar.



| attribute      | Bezeichner                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **Schriftbreite** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Sprachattribute

Informationen zur Sprache des Texts sind über die folgenden Attribute verfügbar.



| attribute              | Bezeichner                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Kultur**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Linkattribut

Das folgende Attribut stellt den Textbereich zur Auswahl, der das Ziel eines Links in einem Dokument ist.



| attribute | Bezeichner                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Link**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Seitenrandattribute

Die umgebundenen Rechtecke eines Textbereichs machen die Koordinaten des Texts auf der Seite nicht verfügbar. Ein Anbieter kann die Seitenrandinformationen jedoch mithilfe der folgenden Textattribute verfügbar machen.



| attribute          | Bezeichner                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Textausrichtungsattribute

Informationen zur Textausrichtung wie Einzug, Registerkarteneinstellungen und horizontale Ausrichtung sind über die folgenden Attribute verfügbar.



| attribute                   | Bezeichner                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **EinzugLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **EinzugTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Registerkarten**                    | [**UIA \_ TabsAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Textfarbattribute

Die Vordergrund- und Hintergrundtextfarben sind über die folgenden Textattribute verfügbar. Beide Farben werden als [**COLORREF-Datentyp**](/windows/desktop/gdi/colorref) angegeben.



| attribute           | Bezeichner                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Textdekorationsattribute

Textdekorationen umfassen Bereiche wie Aufzählungszeichen, Unterstriche und Animationen. Wenn Text führende Aufzählungszeichen oder Zahlen enthält, sollte das Symbol oder der Text, der für das Aufzählungszeichen oder die Zahl verwendet wird, ggf. in den Textstream aufgenommen werden.

Informationen zu Textdekorationen sind über die folgenden Attribute verfügbar.



| attribute              | Bezeichner                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **Bulletstyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Textformatattribute

Informationen zu Textformaten sind über die folgenden Attribute verfügbar.



| attribute         | Bezeichner                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Interaktions- und Auswahlattribute

Informationen zur aktuellen Textauswahl im Bereich und Fokuszustand sind über die folgenden Attribute verfügbar.



| attribute              | Bezeichner                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen zu Benutzeroberflächenautomatisierung Text- und TextRange-Steuerelementmustern](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 