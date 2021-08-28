---
title: SemanticZoom-Steuerelementtyp
description: Dieses Thema enthält Informationen zu Benutzeroberflächenautomatisierung Unterstützung für den SemanticZoom-Steuerelementtyp.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Benutzeroberflächenautomatisierung,Unterstützung für den SemanticZoom-Steuerelementtyp
- Benutzeroberflächenautomatisierung,SemanticZoom-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Struktur für semanticZoom-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Eigenschaften für den SemanticZoom-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Steuerelementmuster für den SemanticZoom-Steuerelementtyp
- Benutzeroberflächenautomatisierung,Events für den SemanticZoom-Steuerelementtyp
- Strukturstrukturen,SemanticZoom-Steuerelementtyp
- properties,SemanticZoom-Steuerelementtyp
- Steuerelementmuster,SemanticZoom-Steuerelementtyp
- events,SemanticZoom-Steuerelementtyp
- Unterstützung für den SemanticZoom-Steuerelementtyp
- SemanticZoom-Steuerelementtyp
- Steuerelementtypen,Struktur für SemanticZoom-Steuerelementtyp
- Steuerelementtypen,Steuerelementmuster für SemanticZoom-Steuerelementtyp
- Steuerelementtypen,Unterstützung für SemanticZoom
- Steuerelementtypen, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9673c5e9beb0c78ecc7dfccc10b6716d6d3afa3f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467757"
---
# <a name="semanticzoom-control-type"></a>SemanticZoom-Steuerelementtyp

Dieses Thema enthält Informationen zu Benutzeroberflächenautomatisierung Unterstützung für den **SemanticZoom-Steuerelementtyp.**

Semantischer Zoom ist eine in Windows 8 eingeführte Technik zum Präsentieren und Navigieren in großen Sätzen verwandter Daten oder Inhalte in einer einzelnen Ansicht, z. B. einem Fotoalb, einer App-Liste oder einem Adressbuch. Der semantische Zoom verwendet zwei unterschiedliche Klassifizierungsmodi oder *Zoomstufen* zum Organisieren und Präsentieren des Inhalts. Im modus low-level (oder *zoomed in*) werden Elemente in einer flachen,"all-up"-Struktur angezeigt. und der modus high-level (oder *zoomed out)* zeigt Elemente in Gruppen an, sodass der Benutzer schnell durch den Inhalt navigieren und navigieren kann. Beispielsweise kann sich das Zoomen einer Liste von Städte in eine Liste von Bundesstaaten ändern, die diese Städte enthalten. Das Zoomen einer Liste von Programmen kann sich in eine Liste logischer Programmgruppen ändern.

Weitere Informationen zum semantischen Zoom, der speziell für Windows Store-Apps verwendet wird, finden Sie unter [Richtlinien für semantischen Zoom.](/windows/uwp/controls-and-patterns/semantic-zoom)

Das Verwendungsmodell für den **SemanticZoom-Steuerelementtyp** ist ungewöhnlich, da es hauptsächlich für den programmgesteuerten Zugriff vorhanden ist. Microsoft Benutzeroberflächenautomatisierung clients can monitor and manipulate the Semantic Zoom control to control the zoomed in state of the list. Benutzer, die keine Hilfstechnologie verwenden, bearbeiten das Steuerelement Semantic Zoom in der Regel direkt über Touchgesten oder Tastenkombinationen.

In den folgenden Abschnitten werden die Benutzeroberflächenautomatisierung Struktur, Eigenschaften, Steuerelementmuster und Ereignisse für den **SemanticZoom-Steuerelementtyp** definiert. Die Benutzeroberflächenautomatisierung gelten für alle Steuerelemente des semantischen Zooms, bei denen das Benutzeroberflächenframework bzw. die Plattform Benutzeroberflächenautomatisierung Unterstützung für Steuerelementtypen und Steuerelementmuster integriert.

Dieses Thema enthält folgende Abschnitte:

-   [Typische Strukturstruktur](#typical-tree-structure)
-   [Relevante Eigenschaften](#relevant-properties)
-   [Erforderliche Steuerelementmuster und -eigenschaften](#required-control-patterns-and-properties)
-   [Erforderliche Ereignisse](#required-events)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Strukturstruktur

Die folgende Tabelle zeigt ein typisches Steuerelement und eine Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur, die sich auf den **SemanticZoom-Steuerelementtyp** bezieht, und beschreibt, was in jeder Ansicht enthalten sein kann. Weitere Informationen zur Struktur Benutzeroberflächenautomatisierung Struktur finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>List<ul><li>[SemanticZoom]<ul><li>ListItem (beliebige Anzahl)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>ListItem (beliebige Anzahl)</li></ul></li></ul> | 




 

Oder:




| Steuerelementansicht | Inhaltsansicht | 
|--------------|--------------|
| <ul><li>[SemanticZoom]<ul><li>List<ul><li>ListItem (beliebige Anzahl)</li></ul></li></ul></li></ul> | <ul><li>List<ul><li>ListItem (beliebige Anzahl)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind Benutzeroberflächenautomatisierung Eigenschaften aufgeführt, deren Wert oder Definition für die Steuerelemente, die den **SemanticZoom-Steuerelementtyp** implementieren, besonders relevant ist. Weitere Informationen zu Eigenschaften Benutzeroberflächenautomatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements.](uiauto-propertiesforclients.md)




| Benutzeroberflächenautomatisierungs-Eigenschaft | Wert | Hinweise | 
|------------------------|-------|-------|
| <a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a> | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peerelemente in der rohen Ansicht der Benutzeroberflächenautomatisierung sein. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a> | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a> | Siehe Hinweise. | Wenn das Listensteuer steuerelement über einen klickbaren Punkt verfügt (ein Punkt, auf den geklickt werden kann, damit die Liste den Fokus besitzt), muss dieser Punkt über diese Eigenschaft verfügbar gemacht werden. Wenn der Wert der <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> TRUE <strong>ist,</strong>führt der Versuch, diese Eigenschaft abzurufen, zum <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> Fehler. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a> | <strong>SemanticZoom</strong> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a> | FALSE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a> | Siehe Hinweise. | Wenn es eine statische Textbezeichnung gibt, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a> | Siehe Hinweise. | Eine lokalisierte Zeichenfolge, die dem <strong>SemanticZoom-Steuerelementtyp</strong> entspricht. Der Standardwert ist "semantischer Zoom" für en-US oder Englisch (USA).<blockquote>[!Note]<br />Einige Frameworks verketteten dies als "semanticzoom".</blockquote><br /> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a> | Siehe Hinweise. | Eine leere Zeichenfolge ist akzeptabel, oder es kann ein nützlicherer Name angegeben werden, solange er nicht den Begriff semantischen Zoom enthält, was die Kombination aus Steuerelementtyp und Name verwirrend machen würde. | 




 

## <a name="required-control-patterns-and-properties"></a>Erforderliche Steuerelementmuster und -eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung, die von allen Steuerelementen für den semantischen Zoom unterstützt werden müssen. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Steuerelementmuster/Mustereigenschaft                  | Unterstützung/Wert | Hinweise                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depends (Abhängig)       | Steuerelemente für semantischen Zoom unterstützen das [Steuerelementmuster](uiauto-implementingtoggle.md) Umschalten, damit der Zoom aktiviert oder deaktiviert werden kann. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht dem flachen All-Up-Zustand, und [**ToggleState \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) entspricht der ansicht mit hoher Vergrößerung. |



 

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierung aufgeführt, die von Semantic Zoom-Steuerelementen unterstützt werden müssen. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).



| Benutzeroberflächenautomatisierung-Ereignis                                                                                                                   | Hinweise                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ BoundingRectanglePropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ IsEnabledPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)                 | Wenn das Steuerelement die [**IsEnabled-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen.   |
| [**UIA \_ IsOffscreenPropertyId-Eigenschaftsänderungsereignis.**](uiauto-automation-element-propids.md)             | Wenn das Steuerelement die [**IsOffscreen-Eigenschaft unterstützt,**](uiauto-automation-element-propids.md) muss es dieses Ereignis unterstützen. |
| [**UIA \_ ToggleToggleStatePropertyId-Eigenschaftsänderungsereignis.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Wenn eine Benutzeroberfläche über eine sichtbare Schaltfläche zum Umschalten des Verhaltens des semantischen Zoomsteuerelementes verfügt, sollte diese Schaltfläche keinen **SemanticZoom-Steuerelementtyp** haben. Dies ist counter-intuitive, aber der **SemanticZoom-Steuerelementtyp** kennzeichnet den Container des zoomenden Inhalts, nicht eine Schaltfläche, die den Zoom steuert. (Eine solche Schaltfläche kann einfach [](uiauto-supportbuttoncontroltype.md) als Button-Steuerelementtyp mit dem [Steuerelementmuster Umschalten](uiauto-implementingtoggle.md) dargestellt werden.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
</dt> </dl>

 

