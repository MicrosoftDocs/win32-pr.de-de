---
title: Bild Steuerelement-Typ
description: Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp "Image".
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- Benutzeroberflächenautomatisierungs, Unterstützung für Bild Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Bild Steuerelement-Typ
- UI-Automatisierung, Baumstruktur für Bild Steuerelement Typen
- Benutzeroberflächenautomatisierungs, Eigenschaften für den Bild Steuerungstyp
- Benutzeroberflächenautomatisierungs, Steuerelement Muster für den Bild Steuerungstyp
- Benutzeroberflächenautomatisierungs, Ereignisse für den Bild Steuerungstyp
- Struktur Strukturen, Bild Steuerelement-Typ
- Eigenschaften, Bild Steuerelement-Typ
- Steuerelement Muster, Bild Steuerelement-Typ
- Ereignisse, Bild Steuerelement-Typ
- Unterstützung für den Bild Steuerungstyp
- Image-Steuerelementtyp
- Steuerelement Typen, Baumstruktur für Bild Steuerelement Typen
- Steuerelement Typen, Steuerelement Muster für den Bild Steuerungstyp
- Steuerelement Typen, Unterstützung für Bild
- Steuerelement Typen, Bild
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "106341484"
---
# <a name="image-control-type"></a>Bild Steuerelement-Typ

Dieses Thema enthält Informationen zur Unterstützung der Microsoft-Benutzeroberflächen Automatisierung für den Steuer ungstyp " **Image** ".

Bild Steuerelemente, die als Symbole, Informationsgrafiken und Diagramme verwendet werden, unterstützen den Steuerelement Typ " **Image** ". **Steuerelemente** , die als Hintergrund-oder Wasserzeichen Bilder verwendet werden, unterstützen den Steuerelement-Steuerelement nicht

In den folgenden Abschnitten werden die erforderliche Benutzeroberflächenautomatisierungs-Struktur, Eigenschaften, Steuerelement Muster und Ereignisse für den **Bild** Steuerelement-Typ definiert. Die Benutzeroberflächenautomatisierungs-Anforderungen gelten für alle Image-Steuerelemente, bei denen Benutzeroberflächen-Framework/Plattform die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelement Typen

Dieses Thema enthält folgende Abschnitte:

- [Typische Baumstruktur](#typical-tree-structure)
- [Relevante Eigenschaften](#relevant-properties)
- [Erforderliche Steuerelement Muster](#required-control-patterns)
- [Erforderliche Ereignisse](#required-events)
- [Zugehörige Themen](#related-topics)

## <a name="typical-tree-structure"></a>Typische Baumstruktur

In der folgenden Tabelle wird eine typische Steuerelement-und Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur für Image-Steuerelemente sowie die möglichen Inhalte der Ansichten beschrieben. Weitere Informationen zur Benutzeroberflächenautomatisierungs-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

| Steuerelementansicht | Inhaltsansicht |
| ------------ | ------------ |
| Image | Bild (abhängig davon, ob das Bild Informationen enthält, basierend auf dem Wert der Eigenschaft [Identifiers der Automatisierungs Element Eigenschaft](uiauto-automation-element-propids.md) ) |

## <a name="relevant-properties"></a>Relevante Eigenschaften

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Eigenschaften aufgelistet, deren Wert oder Definition für die Bild Steuerelemente besonders relevant ist. Weitere Informationen zu Eigenschaften von Benutzeroberflächen Automatisierung finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).

| Benutzeroberflächenautomatisierungs-Eigenschaft                                                                                              | Wert      | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationidpropertyid**](uiauto-automation-element-propids.md)                 | Siehe Hinweise. | Der Wert dieser Eigenschaft muss für alle Peer Elemente in der unformatierten Ansicht der Benutzeroberflächenautomatisierungs-Struktur eindeutig sein.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ boundingrechglepropertyid**](uiauto-automation-element-propids.md)       | Siehe Hinweise. | Das äußere Rechteck, das das gesamte Steuerelement enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ clickablepointpropertyid**](uiauto-automation-element-propids.md)             | Siehe Hinweise. | Der durch Klicken aktivierbare Punkt des Image-Steuer Elements muss ein Punkt innerhalb des umgebenden Rechtecks des Image-Steuer Elements sein.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ controltypepropertyid**](uiauto-automation-element-propids.md)                   | **Image**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)                         | Siehe Hinweise. | Die **HelpText** -Eigenschaft macht eine lokalisierte Zeichenfolge verfügbar, die die tatsächliche visuelle Darstellung des Steuer Elements oder andere dem Bild zugeordnete QuickInfo-Informationen beschreibt. Diese Eigenschaft muss unterstützt werden, wenn eine lange Beschreibung erforderlich ist, um weitere Informationen zum Image-Steuerelement zu vermitteln (z. b. wenn das Bild ein kompliziertes Diagramm oder Diagramm ist). Diese Eigenschaft wird dem HTML **longdesc** -Tag und dem SVG- **DESC** -Tag (Scalable Vector Graphics) zugeordnet. Mit Image-Steuerelementen arbeitende Entwickler müssen eine Eigenschaft unterstützen, um das Festlegen der visuellen Beschreibung für das Steuerelement zu gestatten. Diese Eigenschaft muss der **VisualDescription** -Eigenschaft der Benutzeroberflächen Automatisierung zugeordnet werden. |
| [**UIA \_ iscontentelementpropertyid**](uiauto-automation-element-propids.md)         | Siehe Hinweise. | Das Image-Steuerelement muss in der Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten sein, wenn es aussagekräftige Informationen enthält, die dem Endbenutzer noch nicht verfügbar gemacht wurden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ iscontrolelementpropertyid**](uiauto-automation-element-propids.md)         | TRUE       | Das Image-Steuerelement ist immer in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ iskeyboardfocus ablepropertyid**](uiauto-automation-element-propids.md)   | Siehe Hinweise. | Wenn das Steuerelement den Tastaturfokus erhalten kann, muss es diese Eigenschaft unterstützen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                     | Siehe Hinweise. | Wenn das Image-Steuerelement Statusinformationen zu einem bestimmten Element auf dem Bildschirm darstellt, sollte das Steuerelement in diesem Element enthalten sein. Wenn das Bild in einem Element enthalten ist, muss das Element die Status-Eigenschaft unterstützen und entsprechende Benachrichtigungen beim Status ändern. Wenn ein Bild ein eigenständiges Steuerelement ist und den Status übermittelt, muss diese Eigenschaft unterstützt werden.                                                                                                                                                                                                                                                                                    |
| [**UIA \_ labeledbypropertyid**](uiauto-automation-element-propids.md)                       | Siehe Hinweise. | Wenn eine statische Text Bezeichnung vorhanden ist, muss diese Eigenschaft einen Verweis auf dieses Steuerelement verfügbar machen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) | Siehe Hinweise. | Lokalisierte Zeichenfolge für den Steuer Zeichentyp " **Image** ". Der Standardwert ist "Image" für en-US oder Englisch (USA).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA- \_ namepropertyid**](uiauto-automation-element-propids.md)                                 | Siehe Hinweise. | Die **Name** -Eigenschaft muss für alle Image-Steuerelemente verfügbar gemacht werden, die Informationen enthalten. Der programmgesteuerte Zugriff auf diese Informationen erfordert, dass eine aus Text bestehende Entsprechung zur Grafik bereitgestellt wird. Wenn das Image-Steuerelement rein dekorativ ist, muss es nur in der Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden, und es ist kein Name erforderlich (siehe [Hinweise](#remarks)). Benutzeroberflächenframeworks müssen eine ALT- oder alternative Texteigenschaft für Bilder unterstützen, die innerhalb des Frameworks festgelegt werden kann. Diese Eigenschaft wird dann der Benutzeroberflächenautomatisierungs-Name-Eigenschaft zugeordnet.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Erforderliche Steuerelement Muster

In der folgenden Tabelle werden die Steuerelement Muster für die Benutzeroberflächen Automatisierung aufgelistet, die für Bild Steuerelemente unterstützt werden Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

| Steuerelementmuster                                                 | Support | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Depends (Abhängig) | Das Image-Steuerelement unterstützt das [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster, wenn sich das Steuerelement innerhalb eines Raster Containers befindet.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nie   | Wenn das Image-Steuerelement ein durch Klicken Aktivier bares Objekt ist, sollte das Steuerelement einen Steuerelement Typen unterstützen [, der das](uiauto-supportbuttoncontroltype.md) [Aufruf](uiauto-implementinginvoke.md) Steuerelement Muster unterstützt, z. b. den Steuer Bei einem Bild Objekt, das mehrere durch Klicken aktivierbare Objekte enthält, kann das-Element (Image-Steuer Elementtyp) untergeordnete Links ([Hyperlink](uiauto-supporthyperlinkcontroltype.md) -Steuer Elementtyp) in der Benutzeroberflächenautomatisierungs-Struktur |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Nie   | Image-Steuerelemente sollten das [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Muster nicht unterstützen. Wenn Bilder Teil eines Containers sind, der auswählbar ist, z. b. eine Schaltfläche mit einem Bildsymbol als Inhalt, unterstützt dieser Container das Muster, nicht das Bild in.                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Depends (Abhängig) | Das Image-Steuerelement unterstützt das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster, wenn sich das Steuerelement innerhalb eines Containers befindet, der Header Steuerelemente                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Erforderliche Ereignisse

In der folgenden Tabelle sind die Benutzeroberflächenautomatisierungs-Ereignisse aufgeführt, die von Image-Steuerelementen unterstützt werden Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

| Benutzeroberflächen-Automatisierungs Ereignis                                                                                                                   | Notizen                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ automationfocuschangedebug-ID**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Boundingrechglepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis. |                                                                                                                            |
| [**UIA \_ Isenabledpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                 | Wenn das Steuerelement die [**isaktivierte**](uiauto-automation-element-propids.md) Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.   |
| [**UIA \_ Isoffscreenpropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.             | Wenn das Steuerelement die [**IsOffscreen**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen. |
| [**UIA \_ Itemstatuspropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.               | Wenn das Steuerelement die [**ItemStatus**](uiauto-automation-element-propids.md) -Eigenschaft unterstützt, muss es dieses Ereignis unterstützen.  |
| [**UIA \_ Namepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft-geändertes Ereignis.                           |                                                                                                                            |
| [**UIA \_ structurechangedebug**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Bemerkungen

Der World Wide Web Consortium (W3C) definiert ein dekoratives Bild als eines, das dem Inhalt einer Seite keine Informationen hinzufügt. Weitere Details finden Sie im W3C-Thema zu [dekorativen Images](https://www.w3.org/WAI/tutorials/images/decorative/).

In Bezug auf die Benutzeroberflächen Automatisierung:

- Wenn ein Bild rein dekorativ ist, nicht interaktiv ist und keine Informationen vermittelt, ist das Bild:
  - Kann oder nicht in der UIA-Struktur sein.
  - Kann oder nicht in der UIA-rohansicht sein.
  - Darf nicht in der UIA-Steuerelement Ansicht sein.
  - Darf nicht in der Inhaltsansicht sein.
  - Kann oder keinen Namen haben.
- Wenn ein Bild Informationen vermittelt, aber eindeutig zugeordneter Text vorhanden ist, der die gleichen Informationen bereitstellt (z. b. eine Wiedergabe Schaltfläche, die eine nach links zeigenden Dreieck-Grafik zusammen mit dem Text "Play" enthält), wird das Bild als dekorativ betrachtet und das Bild:
  - Muss sich in der unformatierten Ansicht befinden
  - Muss sich in der Steuerelement Ansicht befinden
  - Darf nicht in der Inhaltsansicht sein.
  - Könnte einen Wert in der Name-Eigenschaft aufweisen.
  - Der Text, der auch die Bedeutung des Bilds vermittelt, muss in der Inhaltsansicht angezeigt werden.
- Wenn ein Bild informativ ist und Details vermittelt, die von keinem zugeordneten Text bereitgestellt werden, wird das Bild:
  - Muss sich in der unformatierten Ansicht befinden
  - Muss sich in der Steuerelement Ansicht befinden
  - Muss sich in der Inhaltsansicht befinden
  - Muss einen namens Wert aufweisen, der das Bild und seine Bedeutung beschreibt.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="conceptual"></a>Konzept

- [Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
- [Übersicht über die Benutzeroberflächenautomatisierung](uiauto-uiautomationoverview.md)
