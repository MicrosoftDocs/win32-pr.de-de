---
title: Informationen zu den Text- und TextRange-Steuerelementmustern
description: Der Textinhalt eines Steuerelements wird mithilfe des Text-Steuerelementmusters verfügbar gemacht, das den Inhalt eines Textcontainers als Textstream darstellt.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Benutzeroberflächenautomatisierung,Textinhaltsunterstützung
- Benutzeroberflächenautomatisierung,Übersicht über Textmuster
- Benutzeroberflächenautomatisierung,Übersicht über Textsteuerelemente
- Benutzeroberflächenautomatisierung,Text-Steuerelementmuster
- Benutzeroberflächenautomatisierung,Textdienstframework (TSF)
- Benutzeroberflächenautomatisierung,TSF
- Benutzeroberflächenautomatisierung,Leistung
- Textmuster,About
- Textmuster,Textdienstframework (TSF)
- Textsteuerelemente, Informationen
- Textinhalt,Unterstützung für
- Textsteuerelemente,Leistung
- Textsteuermuster
- Steuerelementmuster, Text
- Textdienstframework (Text Services Framework, TSF)
- TSF (Textdienstframework)
- Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04112e0233db056c5ff3e81b68256229aa45f60cfdb1258e565e10aea1cd43ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052358"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Informationen zu den Text- und TextRange-Steuerelementmustern

Der Textinhalt eines Steuerelements wird [](uiauto-implementingtextandtextrange.md) mithilfe des Text-Steuerelementmusters verfügbar gemacht, das den Inhalt eines Textcontainers als Textstream darstellt. Das Text-Steuerelementmuster erfordert die Unterstützung des TextRange-Steuerelementmusters, um Format- und Stilattribute verfügbar zu machen. Das TextRange-Steuerelementmuster unterstützt das Text-Steuerelementmuster, indem es zusammenhängende oder mehrere, unzusammenhängende Textbereiche (oder Bereiche) in einem Textcontainer mit einer Auflistung von Start- und Endendpunkten darstellt. Das TextRange-Steuerelementmuster unterstützt Funktionen wie Auswahl, Vergleich, Abruf und Durchlauf.

> [!Note]  
> Das [](uiauto-implementingtextandtextrange.md) Text-Steuerelementmuster bietet keine Möglichkeit zum Einfügen oder Ändern von Text. Je nach Steuerelement kann dies jedoch mithilfe des Microsoft [](uiauto-implementingvalue.md) Benutzeroberflächenautomatisierung Value-Steuerelementmusters oder über direkte Tastatureingaben erreicht werden. Es gibt auch ein [**TextEdit-Muster,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) das programmgesteuerte Änderungen an Text unterstützt.

 

Die in diesem Thema beschriebene Funktionalität ist für Technologieanbieter und deren Endbenutzer von entscheidender Bedeutung. Hilfstechnologien können Benutzeroberflächenautomatisierung verwenden, um vollständige Textformatierungsinformationen für den Benutzer zu sammeln und programmgesteuerte Navigation und Auswahl von Text durch [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (Zeichen, Wort, Zeile oder Absatz) zu ermöglichen.

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächenautomatisierung TextPattern und Textdienstframework](#ui-automation-textpattern-and-the-text-services-framework)
-   [Steuerelementtypen](#control-types)
-   [Anbieterschnittstellen](#provider-interfaces)
-   [Clientschnittstellen](#client-interfaces)
-   [Leistung](#performance)
-   [Textmuster und virtualisierte eingebettete Objekte](#text-pattern-and-virtualized-embedded-objects)
-   [Verwenden des benutzerdefinierten Steuerelementtyps mit dem Textsteuermuster](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Lebensdauer eines Textbereichs](#lifetime-of-a-text-range)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Benutzeroberflächenautomatisierung TextPattern und Textdienstframework

Textdienstframework (TSF) ist ein einfaches und skalierbares Systemframework, das Dienste in natürlicher Sprache und erweiterte Texteingaben auf dem Desktop und in Anwendungen ermöglicht. Zusätzlich zur Bereitstellung von Schnittstellen für Anwendungen, um ihren Textspeicher verfügbar zu machen, werden auch Metadaten für den Textspeicher unterstützt.

TSF wurde für Anwendungen entwickelt, die Eingaben in kontextorientierte Szenarien einjizieren müssen. Das [](uiauto-implementingtextandtextrange.md) Text-Steuerelementmuster ist jedoch eine schreibgeschützte Lösung, die optimierten Zugriff auf einen Textspeicher für Sprachlesegeräte und Braille-Geräte bieten soll.

Barrierefreie Technologien, die schreibgeschützten Zugriff auf einen Textspeicher erfordern, können das Text-Steuerelementmuster verwenden, benötigen jedoch die Funktionalität von TSF für kontextorientierte Eingaben.

Weitere Informationen finden Sie unter [Textdienstframework](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Steuerelementtypen

Die Benutzeroberflächenautomatisierung [Edit-Steuerelementtyp](uiauto-supporteditcontroltype.md) und [Document-Steuerelementtyp](uiauto-supportdocumentcontroltype.md) müssen das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützen. Zur Verbesserung der Barrierefreiheit empfiehlt Microsoft, dass die [Steuerelementtypen QuickInfo](uiauto-supporttooltipcontroltype.md) und Text auch das Text-Steuerelementmuster unterstützen, dies ist jedoch nicht erforderlich.

## <a name="provider-interfaces"></a>Anbieterschnittstellen

Benutzeroberflächenautomatisierung-Anbieter unterstützen das [](uiauto-implementingtextandtextrange.md) Text-Steuerelementmuster für ein Steuerelement, indem sie die [**Schnittstellen ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) implementieren. Diese Schnittstellen machen detaillierte Attributinformationen für Text im Steuerelement verfügbar und bieten stabile Navigationsfunktionen.

Ein Anbieter muss nicht alle Textattribute unterstützen, wenn das Steuerelement keine Unterstützung für ein bestimmtes Attribut hat.

Ein Anbieter muss die [**Methoden ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) und [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) unterstützen, wenn das Steuerelement die Textauswahl oder Platzierung des Textcursors (oder Systemcursors) innerhalb des Textbereichs unterstützt. Wenn das Steuerelement diese Funktionalität nicht unterstützt, muss es keine dieser Methoden unterstützen. Das Steuerelement muss jedoch den Typ der unterstützten Textauswahl verfügbar machen, indem es die [**ITextProvider::SupportedTextSelection-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) implementiert.

Ein Anbieter muss immer die [**TextUnit-Konstanten TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) **\_ Character** und **TextUnit \_ Document** sowie alle anderen unterstützen, die er unterstützen kann.

> [!Note]  
> Der Anbieter kann die Unterstützung für eine bestimmte [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) überspringen, indem er die nächste größte Einheit zurückstelle, die in der folgenden Reihenfolge unterstützt wird: **\_ TextUnit-Zeichen,** **\_ TextUnit-Format,** **TextUnit \_ Word,** **TextUnit \_ Line, TextUnit-Absatz,** **\_ TextUnit-Seite** und **TextUnit-Dokument \_**. **\_**

 

## <a name="client-interfaces"></a>Clientschnittstellen

Benutzeroberflächenautomatisierung Clientanwendungen verwenden die [**Schnittstellen IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) und [**IUIAutomationTextRange,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) um auf den Textinhalt eines Textsteuerfelds zu zugreifen. Clients verwenden **IUIAutomationTextPattern,** um Textbereiche mit dem Namen *Textbereiche* auszuwählen und Zeiger auf **IUIAutomationTextRange-Schnittstellen** für die Bereiche abzurufen. Die **IUIAutomationTextRange-Schnittstelle** ermöglicht Clients das Bearbeiten des Textbereichs und das Abrufen von Informationen über den Text im Bereich, einschließlich Attributen wie Schriftartname, Vordergrundfarbe, Unterstreichungsstil und so weiter. Weitere Informationen finden Sie unter [Textattributbezeichner.](uiauto-textattribute-ids.md)

## <a name="performance"></a>Leistung

Das  Text-Steuerelementmuster basiert für den Großteil seiner Funktionalität auf prozessübergreifenden Aufrufen, sodass es keinen Zwischenspeicherungsmechanismus zur Verbesserung der Leistung bei der Verarbeitung von Inhalten bietet. Auf andere Steuerelementmuster in Microsoft Benutzeroberflächenautomatisierung kann mithilfe der [**IUIAutomationElement::GetCachedPattern-Methode zugegriffen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) werden.

Eine Technik zur Verbesserung der Leistung besteht in der Sicherstellung Benutzeroberflächenautomatisierung dass Clients versuchen, textblöcke mittlerer Größe mithilfe der [**IUIAutomationTextRange::GetText-Methode abzurufen.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) Beispielsweise führt die Verwendung von **GetText** zum Abrufen einzelner Zeichen zu prozessübergreifenden Treffern für jedes Zeichen, während die Angabe einer maximalen Länge beim Aufrufen von **GetText** einen prozessübergreifenden Treffer nach sich geht, aber je nach Größe des Textbereichs eine hohe Latenz haben kann.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Textmuster und virtualisierte eingebettete Objekte

Wenn möglich, sollte eine Anbieterimplementierung von [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) den gesamten Text eines Dokuments unterstützen, einschließlich aller Texte außerhalb des Viewports. Für Text im Off-Screen-Bereich oder eingebettete Objekte, die virtualisiert sind, sollten Anbieter das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) [**(IVirtualizedItemProvider) unterstützen.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)

Wenn ein Dokument virtualisiert wird, während der gesamte Textstream noch verfügbar ist, ruft die [**ITextProvider::D ocumentRange-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) einen Textbereich ab, der das gesamte Dokument enthält. Durch aufrufen der [**ITextRangeProvider-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) wird jedoch eine Auflistung virtualisierter Objekte abgerufen, die alle eingebetteten Objekte im Dokument darstellen. Um mit einem virtualisierten eingebetteten Objekt zu interagieren, müssen Clients die [**IVirtualizedItemProvider::Realize-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufrufen, die den vollständigen Zugriff auf die Elemente als Benutzeroberflächenautomatisierung macht. Clients müssen einen ähnlichen Prozess befolgen, um mit Rasterelementen in einer eingebetteten Tabelle zu arbeiten, bei der ein Teil der Tabelle nicht auf dem Bildschirm angezeigt und virtualisiert ist.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Verwenden des benutzerdefinierten Steuerelementtyps mit dem Textsteuermuster

Das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt zwar viele Textattribute und eingebettete Objekte, es ist jedoch nicht möglich, im Voraus alle möglichen Dokumentelemente und Präsentationstypen zu definieren. Für Dokumentelemente, die von den vorhandenen Attributen oder Standardsteuerelementen nicht unterstützt werden, können Anbieter die Erweiterbarkeitsfunktionen verwenden, die vom Benutzeroberflächenautomatisierung **Steuerelementtyp** bereitgestellt werden.

Bei Anwendungen und Benutzeroberflächen, die auf Seitenpräsentationen basieren, kann die Begrenzungs- und Layoutdarstellung von "Page" auch als eingebettetes Objekt ausgedrückt werden, das über einen benutzerdefinierten Steuerelementtyp (d. h. ) `LocalizedControlType="page"` verfügt. Auf diese Weise kann das eingebettete Objekt andere Seitenelemente hosten, die nicht einfach Teil des Dokumenttextstreams sein können, z. B. die Kopf- und Fußzeilenfelder jeder Seite, als children des eingebetteten "page"-Objekts. Alternativ kann jedes "Page"-Objekt [](uiauto-implementingtextandtextrange.md) das Text-Steuerelementmuster unabhängig voneinander unterstützen, was gut für Anwendungen wie Erstellungstools für Präsentationspräsentationen oder seitenbasierte Desktopveröffentlichungsumgebungen geeignet ist.

## <a name="lifetime-of-a-text-range"></a>Lebensdauer eines Textbereichs

Nach Möglichkeit sollte ein Anbieter sicherstellen, dass alle Textänderungen, z. B. Löschungen, Einfügungen und Verschiebevorgänge, im zugeordneten Textbereich widergespiegelt werden. Wenn das Aktualisieren des Textbereichs nicht möglich ist, sollte der Anbieter ein [**UIA \_ \_ TextChangedEventId-Ereignis**](uiauto-event-ids.md) aufrufen, um Clients darüber zu benachrichtigen, dass der Textbereich nicht mehr gültig ist und ein neuer Bereich abgerufen werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Unterstützung Benutzeroberflächenautomatisierung Eingebettete Objekte](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Textdienstframework](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 