---
title: Steuerelementtyp bearbeiten
description: Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den Steuerelementtyp Bearbeiten.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für Steuerelementtyp bearbeiten
- Benutzeroberflächenautomatisierung,Steuerelementtyp bearbeiten
- Benutzeroberflächenautomatisierung,Struktur für Steuerelementtyp bearbeiten
- Benutzeroberflächenautomatisierung,Eigenschaften für Steuerelementtyp bearbeiten
- Benutzeroberflächenautomatisierung,Steuerelementmuster für Steuerelementtyp bearbeiten
- Benutzeroberflächenautomatisierung,Ereignisse für Steuerelementtyp bearbeiten
- Strukturstrukturen,Steuerelementtyp bearbeiten
- Eigenschaften,Steuerelementtyp bearbeiten
- Steuerelementmuster,Steuerelementtyp bearbeiten
- Ereignisse,Steuerelementtyp bearbeiten
- Unterstützung für Steuerelementtyp bearbeiten
- Edit-Steuerelementtyp
- Steuerelementtypen, Struktur für Steuerelementtyp bearbeiten
- Steuerelementtypen,Steuerelementmuster für Steuerelementtyp bearbeiten
- Steuerelementtypen,Unterstützung für Bearbeiten
- Steuerelementtypen,Bearbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476135"
---
# <a name="edit-control-type"></a>Steuerelementtyp bearbeiten

Dieses Thema enthält Informationen zur Unterstützung von Microsoft Benutzeroberflächenautomatisierung für den **Steuerelementtyp Bearbeiten.**

Mit einem Bearbeitungssteuerelement kann ein Benutzer eine einfache Textzeile ohne umfangreiche Formatierungsunterstützung anzeigen und bearbeiten

In den folgenden Abschnitten werden die erforderlichen Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den Bearbeitungssteuerelementtyp definiert. Die Benutzeroberflächenautomatisierung Anforderungen gelten für alle Bearbeitungssteuerelemente, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Struktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster](#required-control-patterns)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Struktur

Die folgende Tabelle zeigt eine typische Steuerelement- und Inhaltsansicht der Benutzeroberflächenautomatisierung Struktur, die sich auf Bearbeitungssteuerelemente bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Benutzeroberflächenautomatisierung-Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>Bearbeiten</li></ul> | <ul><li>Bearbeiten</li></ul> | 




 

Die Steuerelemente, die den **Steuerelementtyp Bearbeiten** implementieren, verfügen in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur immer über 0 Scrollleisten, da es sich um ein einzeiliges Steuerelement handelt. Die einzelne Textzeile wird in einigen Layoutszenarien möglicherweise umgebrochen. Der **Steuerelementtyp Bearbeiten** ist nur für kleine Textmengen vorgesehen.

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für die Bearbeitungssteuerelemente besonders relevant ist. Weitere Informationen zu Benutzeroberflächenautomatisierung Eigenschaften finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).



| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Hinweise                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung-Struktur eindeutig sein.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Das Bearbeitungssteuerelement muss über einen durch Klicken aktivierbaren Punkt verfügen, der den Eingabefokus an den Bearbeitungsbereich des Steuerelements übergibt, wenn ein Benutzer dort mit der Maus klickt.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Bearbeiten**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Bearbeitungssteuerelement ist immer in der Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Das Bearbeitungssteuerelement ist immer in der Steuerelementansicht der Benutzeroberflächenautomatisierung-Struktur enthalten.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Siehe Hinweise. | Muss für Bearbeitungssteuerelemente, die Kennwörter enthalten, auf **TRUE** festgelegt werden. Wenn ein Bearbeitungssteuerelement Kennwörter enthält, kann diese Eigenschaft von einer Sprachausgabe verwendet werden, um zu ermitteln, ob Tastatureingaben bei der Eingabe durch den Benutzer vorgelesen werden sollen.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn dem Steuerelement eine statische Textbezeichnung zugeordnet ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen. Wenn das Textsteuerelement eine Unterkomponente eines anderen Steuerelements ist, ist keine **LabeledBy-Eigenschaft** festgelegt.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge, die dem **Steuerelementtyp Bearbeiten** entspricht. Der Standardwert ist "bearbeiten" für en-US oder Englisch (USA).                                                                                                                                                       |
| [**\_UIA-NamePropertyId**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Der Name des Bearbeitungssteuerelements wird üblicherweise aus einer statischen Textbezeichnung generiert. Wenn keine statische Textbezeichnung vorhanden ist, muss vom Anwendungsentwickler ein Eigenschaftswert für **Name** zugewiesen werden. Die **Name-Eigenschaft** sollte niemals den Textinhalt des Bearbeitungssteuerelements enthalten. |



 

## <a name="required-control-patterns"></a>Erforderliche Steuerelementmuster

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung Steuerelementmuster aufgeführt, die von Bearbeitungssteuerelementen unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                              | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depends (Abhängig)       | Alle Bearbeitungssteuerelemente, die einen numerischen Bereich annehmen, müssen das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) verfügbar machen.                                                                                                                                                                                                                                                                                       |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Siehe Hinweise.    | Diese Eigenschaft muss der kleinste Wert sein, auf den der Inhalt des Bearbeitungssteuerelements festgelegt werden kann.                                                                                                                                                                                                                                                                                                                     |
| [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Siehe Hinweise.    | Diese Eigenschaft muss der größte Wert sein, auf den der Inhalt des Bearbeitungssteuerelements festgelegt werden kann.                                                                                                                                                                                                                                                                                                                      |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Siehe Hinweise.    | Diese Eigenschaft muss die Anzahl der Dezimalstellen angeben, die für den Wert festgelegt werden kann. Wenn das Bearbeitungssteuerzeichen nur ganze Zahlen angibt, muss der **SmallChange-Eigenschaftswert** 1 sein. Wenn das Bearbeitungssteuerprogramm einen Bereich von 1,0 bis 2,0 an nimmt, muss der **SmallChange-Eigenschaftswert** 0,1 sein. Wenn das Bearbeitungssteuerprogramm einen Bereich von 1,00 bis 2,00 an nimmt, muss der **SmallChange-Eigenschaftswert** 0,001 sein.                   |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Diese Eigenschaft muss auf einem Bearbeitungssteuerelement nicht verfügbar gemacht werden.                                                                                                                                                                                                                                                                                                                                                      |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Siehe Hinweise.    | Diese Eigenschaft gibt den numerischen Inhalt des Bearbeitungssteuer steuerelements an. Wenn ein genauerer Wert von einem Benutzeroberflächenautomatisierung-Client innerhalb der in den Eigenschaften [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) und [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) angegebenen Bereiche festgelegt wird, wird die [**Value-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) automatisch auf den nächstgelegenen akzeptierten Wert gerundet. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Erforderlich      | Alle Bearbeitungssteuerelemente [](uiauto-implementingtextandtextrange.md) müssen das Text-Steuerelementmuster unterstützen, da detaillierte Informationen immer für Hilfstechnologieclients verfügbar sein müssen.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depends (Abhängig)       | Alle Bearbeitungssteuerelemente, die eine Zeichenfolge verwenden, müssen das [Value-Steuerelementmuster](uiauto-implementingvalue.md) verfügbar machen.                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Siehe Hinweise.    | Diese Eigenschaft muss festgelegt werden, um anzugeben, ob für das Steuerelement programmgesteuert ein Wert festgelegt werden kann oder ob er vom Benutzer bearbeitet werden kann.                                                                                                                                                                                                                                                                                |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Siehe Hinweise.    | Diese Eigenschaft enthält den Textinhalt des Bearbeitungssteuerfelds. Wenn die [**\_ UIA-Eigenschaft IsPasswordPropertyId**](uiauto-automation-element-propids.md) auf **TRUE** festgelegt ist, muss beim Abfragen der [**Value-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) ein Fehler zurückgegeben werden.                                                                                                                      |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von Bearbeitungssteuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                                        | Hinweise                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                      | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                  | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ NamePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                                                |                                                                                                                            |
| [**UIA \_ RangeValueValuePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)                             | Wenn das Steuerelement das [RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)   | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md) | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ ScrollHorizontalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)           | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ ScrollVerticallyScrollablePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)       | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)     | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ ScrollVerticalViewSizePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)               | Ein Bearbeitungssteuerfeld [](uiauto-implementingscroll.md) unterstützt nie das Bildlauf-Steuerelementmuster.                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      | Wenn das Steuerelement das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    | Wenn das Steuerelement das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ ValueValuePropertyId-Eigenschaftsänderungsereignis**](uiauto-control-pattern-propids.md) .                                      | Wenn das Steuerelement das [Value-Steuerelementmuster](uiauto-implementingvalue.md) unterstützt, muss es dieses Ereignis unterstützen.             |



 

## <a name="remarks"></a>Hinweise

Ein Bearbeitungssteuerfeld kann als schreibgeschütztes Textfeld verwendet werden, das die Auswahl oder Bearbeitung von Text nicht unterstützt. Ein solches Bearbeitungssteuerfeld verhält sich wie ein Feldobjekt mit einem bestimmten Namen und Wert.

Wenn ein Bearbeitungssteuerfeld Platzhaltertext enthält (z. B. ein Cue-Banner), sollte der Text als **HelpText-Eigenschaft** verwendet werden, es sei denn, der Text kann vom Benutzer bearbeitet und dann als Platzhaltertext wiederverwendet werden. Die Adressleiste Windows Internet Explorer enthält beispielsweise den Text "about:Tabs", wenn eine neue Registerkarte geöffnet wird. Dies ist **nicht HelpText,** da es sich um eine programmgesteuerte Adresse handelt, die vom Benutzer verwendet oder bearbeitet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




