---
title: Steuerelementtyp "Thumb"
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den Steuerelementtyp Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung des Steuerelementtyps Thumb
- Benutzeroberflächenautomatisierung, Steuerelementtyp "Thumb"
- Benutzeroberflächenautomatisierung,Struktur für den Steuerelementtyp Thumb
- Benutzeroberflächenautomatisierung,Eigenschaften für den Steuerelementtyp Thumb
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den Steuerelementtyp Thumb
- Benutzeroberflächenautomatisierung,Ereignisse für den Steuerelementtyp Thumb
- Strukturstrukturen, Steuerelementtyp "Thumb"
- Properties, Thumb-Steuerelementtyp
- Steuerelementmuster, Steuerelementtyp "Thumb"
- Ereignisse, Steuerelementtyp "Thumb"
- Unterstützung für den Steuerelementtyp Thumb
- Thumb-Steuerelementtyp
- Steuerelementtypen, Struktur für Thumb-Steuerelementtyp
- Steuerelementtypen, Steuerelementmuster für den Steuerelementtyp Thumb
- Steuerelementtypen,Unterstützung für Thumb
- Steuerelementtypen,Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea75b39ae0b17be23886823d446667299e5f0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478786"
---
# <a name="thumb-control-type"></a>Steuerelementtyp "Thumb"

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **Steuerelementtyp Thumb.**

Thumb-Steuerelemente bieten die Funktionen, mit denen ein Steuerelement bewegt (oder gezogen) werden kann, wie ein Schieberegler für Bildlaufleisten, oder in der Größe angepasst werden kann, wie ein Widget für die Größenanpassung von Fenstern. Beachten Sie, dass ein Ziehpunkt-Steuerelement keine Drag & Drop-Funktionalität bereitstellt. Thumb-Steuerelemente können den Mausfokus empfangen, aber keinen Tastaturfokus. Der Entwickler von Steuerelementen muss das Steuerelement implementieren, damit es entsprechend funktioniert (d. h. es kann gezogen bzw. in der Größe angepasst werden).

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **Steuerelementtyp Thumb** definiert. Die Benutzeroberflächenautomatisierung-Anforderungen wenden alle Thumb-Steuerelemente an, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Thumb-Steuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Ziehpunkt</li></ul> | (Nicht vorhanden) | 




 

Thumb-Steuerelemente werden nie in der Inhaltsansicht angezeigt, da sie nur für die Bearbeitung mit der Maus vorhanden sind. Sie werden über ein anderes Steuerelementmuster verfügbar gemacht, z. [B.](uiauto-implementingscroll.md) das Scroll-Steuerelementmuster, [das Steuerelementmuster Transformieren](uiauto-implementingtransform.md) oder das [RangeValue-Steuerelementmuster,](uiauto-implementingrangevalue.md) das im Container des Steuerelements unterstützt wird.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für Thumb-Steuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Ein Punkt innerhalb des sichtbaren Clientbereichs des Steuerelements thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Daumen**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Das Steuerelement "Thumb" ist nie in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Das Steuerelement thumb ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen. Ein Thumb-Steuerelement kann den Fokus erhalten, wenn es als "Zentrierungsobjekt" zum Dimensionieren eines Fensters oder Bereichs verwendet wird. Ein Schieberegler- oder Bildlaufleisten-Steuerelement sollte nie den Fokus erhalten. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Thumb-Steuerelemente haben niemals eine Bezeichnung.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Thumb entspricht.** Der Standardwert ist "thumb" für en-US oder Englisch (USA).                                                                                                                             |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | Da das Thumb-Steuerelement in der Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur nicht verfügbar ist, ist kein Name erforderlich.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von Thumb-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster                                         | Support  | Notizen                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Erforderlich | Ermöglicht, dass das Ziehpunkt-Steuerelement auf dem Bildschirm bewegt werden kann. Da die Größe des Steuerelements "Thumb" in der Regel nicht geändert oder gedreht werden kann, unterstützt das [Steuerelementmuster Transform](uiauto-implementingtransform.md) in erster Linie die [**Move-Funktion.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Ereignisse aufgeführt, die von Thumb-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Das BoundingRectanglePropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Das IsEnabledPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftswechselereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft**](uiauto-automation-element-propids.md) unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




