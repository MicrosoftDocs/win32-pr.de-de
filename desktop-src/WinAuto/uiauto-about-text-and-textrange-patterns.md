---
title: Informationen zu Text-und TextRange-Steuerelement Mustern
description: Der Text Inhalt eines Steuer Elements wird mit dem Text-Steuerelement Muster verfügbar gemacht, das den Inhalt eines Text Containers als Textstream darstellt.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Benutzeroberflächen Automatisierung, Unterstützung von Textinhalten
- UI-Automatisierung, Übersicht über Textmuster
- UI-Automatisierung, Übersicht über Text Steuerelemente
- UI-Automatisierung, Text-Steuerelement Muster
- UI-Automatisierung, Text Dienste-Framework (TSF)
- UI-Automatisierung, TSF
- Automatisierung der Benutzeroberfläche, Leistung
- Textmuster, Info
- Textmuster, Text Dienste-Framework (TSF)
- Text Steuerelemente, Info
- Text Inhalt, Unterstützung für
- Text Steuerelemente, Leistung
- Text-Steuerelement Muster
- Steuerelement Muster, Text
- Textdienstframework (Text Services Framework, TSF)
- TSF (Text Dienste-Framework)
- Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342374"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Informationen zu Text-und TextRange-Steuerelement Mustern

Der Text Inhalt eines Steuer Elements wird mit dem [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster verfügbar gemacht, das den Inhalt eines Text Containers als Textstream darstellt. Das Text-Steuerelement Muster erfordert die Unterstützung des TextRange-Steuerelement Musters, um Format-und Stil Attribute verfügbar zu machen. Das TextRange-Steuerelement Muster unterstützt das Text-Steuerelement Muster, indem zusammenhängende oder mehrere, nicht zusammenhängende Text spannen (oder Bereiche) in einem Text Container mit einer Auflistung von Start-und endendpunkten dargestellt werden. Das TextRange-Steuerelement Muster unterstützt Funktionen wie Auswahl, Vergleich, Abruf und Durchlauf.

> [!Note]  
> Das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster bietet keine Möglichkeit, Text einzufügen oder zu ändern. Abhängig vom Steuerelement kann dies jedoch mithilfe des Microsoft UI Automation [value](uiauto-implementingvalue.md) -Steuerelement Musters oder durch direkte Tastatureingaben erreicht werden. Außerdem gibt es ein [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) -Muster, das programmgesteuerte Änderungen an Text unterstützt.

 

Die in diesem Thema beschriebene Funktionalität ist wichtig für Hilfstechnologieanbieter und deren Endbenutzer. Hilfstechnologien können die Benutzeroberflächen Automatisierung verwenden, um vollständige Text Formatierungsinformationen für den Benutzer zu erfassen und programmgesteuerte Navigation und Auswahl von Text durch [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (Zeichen, Wort, Zeile oder Absatz) bereitzustellen.

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächenautomatisierungs-TextPattern und das Text Services-Framework](#ui-automation-textpattern-and-the-text-services-framework)
-   [Steuerelementtypen](#control-types)
-   [Anbieterschnittstellen](#provider-interfaces)
-   [Client Schnittstellen](#client-interfaces)
-   [Leistung](#performance)
-   [Text Muster und virtualisierte eingebettete Objekte](#text-pattern-and-virtualized-embedded-objects)
-   [Verwenden des benutzerdefinierten Steuerelement Typs mit dem Text-Steuerelement Muster](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Lebensdauer eines Text Bereichs](#lifetime-of-a-text-range)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Benutzeroberflächenautomatisierungs-TextPattern und das Text Services-Framework

Das Text Services-Framework (TSF) ist ein einfaches und skalierbares System Framework, das Dienste für natürliche Sprachen und erweiterte Texteingaben auf dem Desktop und in Anwendungen ermöglicht. Zusätzlich zur Bereitstellung von Schnittstellen für Anwendungen, um Ihren Text Speicher verfügbar zu machen, unterstützt es auch Metadaten für den Text Speicher.

TSF wurde für Anwendungen entwickelt, die Eingaben in kontextabhängige Szenarien einfügen müssen. Das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster ist jedoch eine schreibgeschützte Lösung, die den optimierten Zugriff auf einen Text Speicher für Sprachausgaben und Braille-Geräte ermöglichen soll.

Barrierefreie Technologien, die schreibgeschützten Zugriff auf einen Text Speicher erfordern, können das Text-Steuerelement Muster verwenden, benötigen aber die Funktionalität von TSF für kontextabhängige Eingaben.

Weitere Informationen finden Sie unter [Text Services-Framework](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Steuerelementtypen

Der Benutzeroberflächenautomatisierungs [-](uiauto-supporteditcontroltype.md) Steuerelement-und dokumentsteuerungstyp muss das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unterstützen. [](uiauto-supportdocumentcontroltype.md) Zur [Verbesserung der Barrierefreiheit](uiauto-supporttooltipcontroltype.md) empfiehlt Microsoft, dass die QuickInfo-und Text Steuerelement Typen auch das Text-Steuerelement Muster unterstützen. Dies ist jedoch nicht erforderlich.

## <a name="provider-interfaces"></a>Anbieterschnittstellen

Benutzeroberflächenautomatisierungs-Anbieter unterstützen das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster für ein Steuerelement durch Implementieren der Schnittstellen [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Diese Schnittstellen machen ausführliche Attributinformationen für Text im-Steuerelement verfügbar und bieten stabile Navigationsfunktionen.

Ein Anbieter muss nicht alle Text Attribute unterstützen, wenn das Steuerelement keine Unterstützung für ein bestimmtes Attribut hat.

Ein Anbieter muss die [**ITextProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) -und [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) -Methode unterstützen, wenn das Steuerelement die Textauswahl oder die Platzierung des Text Cursors (oder der System Einfügemarke) innerhalb des Text Bereichs unterstützt. Wenn das Steuerelement diese Funktionalität nicht unterstützt, muss keines dieser Methoden unterstützt werden. Das Steuerelement muss jedoch den Typ der von ihm unterstützten Textauswahl verfügbar machen, indem er die [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) -Eigenschaft implementiert.

Ein Anbieter muss immer die [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) -Konstanten, das **TextUnit- \_ Zeichen** und das **TextUnit- \_ Dokument** sowie alle anderen unterstützen, die er unterstützen kann.

> [!Note]  
> Der Anbieter kann die Unterstützung für eine [**bestimmte TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) überspringen, indem er auf die nächst größere Einheit, die in der folgenden Reihenfolge unterstützt wird, verzögert wird: **TextUnit- \_ Zeichen**, TextUnit- **\_ Format**, **TextUnit- \_ Wort**, **TextUnit- \_ Textzeile** **, \_** TextUnit- **\_ Seite** und **TextUnit- \_ Dokument**.

 

## <a name="client-interfaces"></a>Client Schnittstellen

Benutzeroberflächenautomatisierungs-Client Anwendungen verwenden die [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) -und die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle für den Zugriff auf den Text Inhalt eines Text Steuer Elements. Clients verwenden **iuiautomationtextpattern** , um Text *Bereiche als Textbereiche* auszuwählen und Zeiger auf **iuiautomationtextrange** -Schnittstellen für die Bereiche abzurufen. Mit der **iuiautomationtextrange** -Schnittstelle können Clients den Textbereich bearbeiten und Informationen über den Text im Bereich abrufen, z. b. Attribute wie Schriftart Name, Vordergrundfarbe, unterstrich Stil usw. Weitere Informationen finden Sie unter [Text Attribut](uiauto-textattribute-ids.md)Bezeichner.

## <a name="performance"></a>Leistung

Das **Text** -Steuerelement Muster basiert auf prozessübergreifenden aufrufen für die meisten Funktionen und stellt daher keinen Cachingmechanismus bereit, um die Leistung beim Verarbeiten von Inhalten zu verbessern. Auf andere Steuerelement Muster in der Microsoft-Benutzeroberflächen Automatisierung kann mithilfe der [**iuiautomationelement:: GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) -Methode zugegriffen werden.

Eine Methode zur Verbesserung der Leistung besteht darin sicherzustellen, dass Benutzeroberflächenautomatisierungs-Clients versuchen, mit der [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) -Methode mittelgroße Textblöcke abzurufen. Wenn Sie z. b. **gettext** zum Abrufen von einzelnen Zeichen verwenden, entstehen prozessübergreifende Treffer für jedes Zeichen, während beim Aufrufen von **gettext** keine maximale Länge festgelegt wird. Dies hängt von der Größe des Text Bereichs ab.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Text Muster und virtualisierte eingebettete Objekte

Wenn möglich, sollten die Anbieter Implementierung von [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) und [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) den gesamten Text eines Dokuments unterstützen, einschließlich Text außerhalb des Viewports. Anbieter sollten das [VirtualizedItem-Steuerelement Muster](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)) unterstützen.

Wenn ein Dokument virtualisiert wird, während der gesamte Textstream weiterhin verfügbar ist, ruft die [**ITextProvider::D ocreentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) -Eigenschaft einen Textbereich ab, der das gesamte Dokument einschließt. Wenn Sie jedoch die [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) -Methode aufrufen, wird eine Auflistung von virtualisierten Objekten abgerufen, die alle eingebetteten Objekte im Dokument darstellen. Um mit einem virtualisierten eingebetteten Objekt zu interagieren, müssen Clients die [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) -Methode aufrufen, um die Elemente vollständig als Benutzeroberflächenautomatisierungs-Elemente zugänglich zu machen. Clients müssen einen ähnlichen Prozess zum Arbeiten mit Raster Elementen in einer eingebetteten Tabelle befolgen, in der ein Teil der Tabelle außerhalb des Bildschirms und virtualisiert ist.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Verwenden des benutzerdefinierten Steuerelement Typs mit dem Text-Steuerelement Muster

Während das [Text](uiauto-implementingtextandtextrange.md) Steuerelement Muster viele Text Attribute und eingebettete Objekte unterstützt, ist es nicht möglich, im Voraus alle möglichen Dokument Elemente und Darstellungs Typen zu definieren. Für Dokument Elemente, die nicht von den vorhandenen Attributen oder Standard Steuerelement Typen unterstützt werden, können Anbieter die Erweiterbarkeits Funktionen verwenden, die vom **benutzerdefinierten** Steuerungstyp Benutzeroberflächenautomatisierung bereitgestellt werden.

Für Anwendungen und Benutzeroberflächen, die auf Seiten Präsentationen basieren, kann die Begrenzung und Layoutdarstellung von "page" auch als eingebettetes Objekt mit einem benutzerdefinierten Steuerelement Typen (d. h `LocalizedControlType="page"` .) ausgedrückt werden. Auf diese Weise kann das eingebettete Objekt andere Seitenelemente hosten, die nicht einfach Teil des Dokument Text Stroms sein können, z. b. die Kopf-und Fußzeilen Felder jeder Seite, als untergeordnete Elemente des eingebetteten "page"-Objekts. Alternativ kann jedes "page"-Objekt das [Text](uiauto-implementingtextandtextrange.md) -Steuerelement Muster unabhängig unterstützen, das für Anwendungen wie z. b. das Erstellen von Bildschirmpräsentationen oder seitenbasierten Desktop Veröffentlichungs Umgebungen gut funktioniert.

## <a name="lifetime-of-a-text-range"></a>Lebensdauer eines Text Bereichs

Wenn möglich, sollte ein Anbieter sicherstellen, dass alle Textänderungen, wie z. b. Löschvorgänge, Einfügungen und Verschiebungen, im zugeordneten Textbereich widergespiegelt werden. Wenn das Aktualisieren des Text Bereichs nicht möglich ist, sollte der Anbieter ein [**UIA \_ Text \_ -textchangedebug-**](uiauto-event-ids.md) Ereignis ausgeben, um Clients zu benachrichtigen, dass der Textbereich nicht mehr gültig ist und eine neue abgerufen werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Unterstützung eingebetteter Objekte durch die Benutzeroberflächen Automatisierung](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Textdienstframework](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 