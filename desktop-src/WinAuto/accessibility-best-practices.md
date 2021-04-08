---
title: Bewährte Methoden für Eingabehilfen
description: Durch das Implementieren der in diesem Abschnitt beschriebenen bewährten Methoden können Sie sicherstellen, dass Ihre Anwendung für Personen zugänglich ist, die Hilfstechnologieprodukte verwenden.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d9f70828610d04255b61ad3ee533d23c514867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855927"
---
# <a name="accessibility-best-practices"></a>Bewährte Methoden für Eingabehilfen

Durch das Implementieren der in diesem Abschnitt beschriebenen bewährten Methoden können Sie sicherstellen, dass Ihre Anwendung für Personen zugänglich ist, die Hilfstechnologieprodukte verwenden. Viele dieser bewährten Methoden konzentrieren sich auf ein gutes Design der Benutzeroberfläche. Jede bewährte Vorgehensweise umfasst Implementierungs Informationen für-Steuerelemente oder-Anwendungen. In vielen Fällen ist der Großteil der Arbeit, um diese bewährten Methoden zu erfüllen, bereits in den Steuerelementen enthalten.

Dieses Thema enthält folgende Abschnitte:

-   [Programm gesteuerter Zugriff](#programmatic-access)
    -   [Aktivieren des programmgesteuerten Zugriffs auf alle Elemente der Benutzeroberfläche und auf Text](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Platzieren von Namen, Titeln und Beschreibungen auf Benutzeroberflächenobjekte, Frames und Seiten](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Gewährleisten der Auslösung programmgesteuerter Ereignisse durch alle Aktivitäten auf der Benutzeroberfläche](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Benutzereinstellungen](#user-settings)
    -   [Respektieren aller systemweiten Einstellungen und Beachten der Barrierefreiheitsfunktionen](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Entwurf der visuellen Benutzeroberfläche](#visual-ui-design)
    -   [Farben nicht Hard-Code](#do-not-hard-code-colors)
    -   [Unterstützen von hohem Kontrast und allen Systemanzeigeattributen](#support-high-contrast-and-all-system-display-attributes)
    -   [Gewährleisten der ordnungsgemäßen Skalierung aller Benutzeroberflächenelemente bei beliebiger DPI-Einstellung](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Tastatur Navigation](#keyboard-navigation)
    -   [Bereitstellen einer Tastaturschnittstelle für alle Elemente der Benutzeroberfläche](#provide-keyboard-interface-for-all-ui-elements)
    -   [Anzeigen des Tastaturfokus](#show-the-keyboard-focus)
    -   [Unterstützen von Navigationsstandards und leistungsstarken Navigationsschemas](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Vermeiden störender Auswirkungen der Mausposition auf die Tastaturnavigation](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Multimodale Schnittstelle](#multi-modal-interface)
    -   [Bereitstellen von auswählbaren Entsprechungen für Nicht-Text-Elemente](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Verwenden von Farbe und Bereitstellen von Alternativen für Farbe](#use-color-but-also-provide-alternatives-to-color)
    -   [Verwenden von Standardeingabe-APIs mit geräteunabhängigen Aufrufen](#use-standard-input-apis-with-device-independent-calls)
-   [Zugehörige Themen](#related-topics)

## <a name="programmatic-access"></a>Programmgesteuerter Zugriff

Mit den bewährten Methoden in diesem Abschnitt wird erläutert, dass Hilfstechnologieprodukte angemessenen programmgesteuerten Zugriff auf Benutzeroberflächen Informationen und-Funktionen haben.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Aktivieren des programmgesteuerten Zugriffs auf alle Elemente der Benutzeroberfläche und auf Text

Die Elemente der Benutzeroberfläche der Anwendung müssen für Hilfstechnologieprodukte Programm gesteuert zugänglich sein. Alle Elemente der Benutzeroberfläche müssen über Bezeichnungen verfügen, Sie müssen alle Eigenschaftswerte verfügbar machen, und Sie müssen alle entsprechenden Ereignisse hervorrufen. Bei den standardmäßigen Windows-Steuerelementen erfolgt der größte Teil dieser Arbeit bereits über die Microsoft-Benutzeroberflächenautomatisierungs-und Microsoft Active Accessibility-Proxy Objekte. Benutzerdefinierte Steuerelemente erfordern jedoch zusätzliche Arbeit, um sicherzustellen, dass Sie vollständig verfügbar gemacht werden, sodass Hilfstechnologieanbieter Elemente Ihrer Anwendungs Benutzeroberfläche identifizieren und bearbeiten können.

Durch Befolgen dieser bewährten Vorgehensweise können Hilfstechnologieanbieter Elemente der Benutzeroberfläche Ihres Produkts identifizieren und bearbeiten.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Platzieren von Namen, Titeln und Beschreibungen auf Benutzeroberflächenobjekte, Frames und Seiten

Da Hilfstechnologieprodukte – besonders Bildschirm Sprachausgaben – Titel verwenden, um die Position eines Frames, Objekts oder einer Seite im Navigations Schema zu verstehen, müssen die Titel sehr aussagekräftig sein. Gute beschreibende Titel ermöglichen Hilfstechnologieprodukten, Benutzeroberflächen Elemente in Steuerelementen und Anwendungen zu identifizieren und zu bearbeiten. Beispielsweise ist der Webseiten Titel "Microsoft-Webseite" nutzlos, wenn der Benutzer tief zu einem bestimmten Bereich navigiert ist. Ein beschreibender Titel ist wichtig für Benutzer, die blind sind und von Bildschirmlesern abhängig sind.

Durch Befolgen dieser bewährten Vorgehensweise können Hilfstechnologieprodukte die Benutzeroberfläche in Beispiel Steuerelementen und-Anwendungen identifizieren und bearbeiten.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Gewährleisten der Auslösung programmgesteuerter Ereignisse durch alle Aktivitäten auf der Benutzeroberfläche

Die Anwendung sollte Ereignisse immer dann ausgelöst werden, wenn im Zustand oder in der Darstellung eines UI-Elements Änderungen auftreten.

Durch Befolgen dieser bewährten Vorgehensweise können Hilfstechnologieprodukte auf Änderungen in der Benutzeroberfläche lauschen und den Benutzer über diese Änderungen benachrichtigen.

## <a name="user-settings"></a>Benutzereinstellungen

Die bewährte Methode in diesem Abschnitt stellt sicher, dass Steuerelemente oder Anwendungen die Benutzereinstellungen nicht außer Kraft setzen.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respektieren aller systemweiten Einstellungen und Beachten der Barrierefreiheitsfunktionen

Benutzer können mit der Systemsteuerung einige systemweite Flags festlegen. andere Flags können Programm gesteuert festgelegt werden. Diese Einstellungen dürfen nicht von Steuerelementen oder Anwendungen geändert werden. Darüber hinaus müssen Anwendungen die Einstellungen für die Barrierefreiheit ihres Hostbetriebssystems unterstützen.

Durch Befolgen dieser bewährten Methode können Benutzer Einstellungen für die Barrierefreiheit festlegen und dadurch wissen, dass diese Einstellungen von Anwendungen nicht geändert werden.

## <a name="visual-ui-design"></a>Entwurf der visuellen Benutzeroberfläche

Die bewährten Methoden in diesem Abschnitt stellen sicher, dass Steuerelemente oder Anwendungen Farben und Bilder effektiv verwenden und von Hilfstechnologieprodukten verwendet werden können.

### <a name="do-not-hard-code-colors"></a>Farben nicht Hard-Code

Personen, die farbenblind sind, eine Sehschwäche aufweisen oder einen monochromen Bildschirm verwenden, können Anwendungen mit hartcodierten Farben möglicherweise nicht verwenden.

Durch Befolgen dieser bewährten Methode können Benutzer die Farbkombinationen auf Grundlage individueller Anforderungen anpassen.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Unterstützen von hohem Kontrast und allen Systemanzeigeattributen

Anwendungen sollten vom Benutzer ausgewählte, systemweite Kontrasteinstellungen, Farbauswahlen oder andere systemweite Anzeigeeinstellungen und -attribute nicht stören oder deaktivieren. Die von einem Benutzer übernommenen systemweiten Einstellungen erhöhen die Barrierefreiheit von Anwendungen, daher sollten sie von Anwendungen nicht deaktiviert oder ignoriert werden. Farben müssen in der richtigen Kombination für Vorder- und Hintergrund verwendet werden, um den geeigneten Kontrast zu bieten. Nicht verbundene Farben sollten nicht kombiniert und Farben nicht invertiert werden.

Viele Benutzer benötigen bestimmte kontrastreiche Kombinationen, z. B. weißen Text auf schwarzem Hintergrund. Die invertierte Darstellung mit schwarzem Text auf weißem Hintergrund führt dazu, dass der Hintergrund auf den Vordergrund übergreift und das Lesen für manche Benutzer erschwert wird.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Gewährleisten der ordnungsgemäßen Skalierung aller Benutzeroberflächenelemente bei beliebiger DPI-Einstellung

Stellen Sie sicher, dass alle Elemente der Benutzeroberfläche durch beliebige dpi-Einstellungen (dpi) ordnungsgemäß skaliert werden können. Stellen Sie außerdem sicher, dass Benutzeroberflächen Elemente in einem Bildschirm von 1024 x 768 mit 120 Punkten pro Zoll (dpi) passen.

## <a name="keyboard-navigation"></a>Tastaturnavigation

Die bewährten Methoden in diesem Abschnitt stellen sicher, dass Benutzer, die auf der Tastatur basieren, auf die gesamte Anwendungs Funktionalität zugreifen können.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Bereitstellen einer Tastaturschnittstelle für alle Elemente der Benutzeroberfläche

Tabstopps, insbesondere wenn Sie sorgfältig geplant sind, haben Benutzern eine weitere Möglichkeit, die Benutzeroberfläche zu navigieren.

Anwendungen sollten die folgenden Tastaturschnittstellen bereitstellen:

-   Tabstopps für alle Steuerelemente, mit denen der Benutzer interagieren kann, z. b. Schaltflächen, Links oder Listenfelder.
-   Logische Aktivier Reihenfolge.

### <a name="show-the-keyboard-focus"></a>Anzeigen des Tastaturfokus

Benutzer müssen wissen, welches Objekt den Tastaturfokus hat, damit sie die Auswirkungen ihrer Tastatureingaben voraussehen können. Verwenden Sie Farben, Schriftarten oder grafische Darstellungen (z. B. Rechtecke oder eine Vergrößerung), um den Tastaturfokus hervorzuheben. Um den Tastaturfokus akustisch hervorzuheben, ändern Sie die Lautstärke, Tonhöhe oder Tonqualität.

Um Verwechselungen zu vermeiden, sollten Anwendungen alle visuellen Fokusindikatoren ausblenden und die Auswahl abblenden, die sich in inaktiven Fenstern (oder Bereichen) befindet.

Anwendungen sollten beim Tastaturfokus wie folgt vorgehen:

-   Ein Element sollte immer über den Tastaturfokus verfügen.
-   Der Tastaturfokus sollte sichtbar und offensichtlich sein.
-   Auswahl und/oder fokussierte Elemente sollten visuell hervorgehoben werden.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Unterstützen von Navigationsstandards und leistungsstarken Navigationsschemas

Verschiedene Aspekte der Tastaturnavigation bieten verschiedene Möglichkeiten für Benutzer, die Benutzeroberfläche zu navigieren.

Anwendungen sollten die folgenden Tastaturschnittstellen bereitstellen:

-   Tastenkombinationen und unterstrichene Zugriffstasten für alle Befehle, Menüs und Steuerelemente.
-   Tastenkombinationen zu wichtigen Links.
-   Alle Menü Elemente verfügen über eine Zugriffstaste. alle Schaltflächen verfügen über Tastenkombinationen, alle Befehle verfügen über eine Zugriffstaste.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Vermeiden störender Auswirkungen der Mausposition auf die Tastaturnavigation

Die Position des Mauszeigers sollte nicht die Tastaturnavigation behindern. Wenn sich der Mauszeiger z. B. an einer beliebigen Position befindet und der Benutzer über die Tastatur navigiert, darf ein Mausklick nur auftreten, wenn er vom Benutzer initiiert wird.

## <a name="multi-modal-interface"></a>Multimodale Schnittstelle

Die bewährte Vorgehensweise in diesem Abschnitt stellt sicher, dass die Benutzeroberfläche der Anwendung Alternativen für visuelle Elemente enthält.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Bereitstellen von auswählbaren Entsprechungen für Nicht-Text-Elemente

Geben Sie für jedes Nicht-Textelement eine vom Benutzer auswählbare Entsprechung für Text, Aufzeichnungen oder Audiobeschreibungen ein, z. B. alternativen Text, Beschriftungen oder visuelles Feedback.

Nicht-Textelemente decken eine breite Palette von Elementen der Benutzeroberfläche ab, einschließlich: Bilder, Imagemapbereiche, Animationen, Applets, Frames, Skripts, grafische Schaltflächen, Sounds, eigenständige Audiodateien und Videos. Nicht-Textelemente sind wichtig, wenn Sie visuelle Informationen, Sprache oder allgemeine Audioinformationen enthalten, auf die der Benutzer Zugriff hat, um den Inhalt der Benutzeroberfläche zu verstehen.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Verwenden von Farbe und Bereitstellen von Alternativen für Farbe

Verwenden Sie Farbe, um Informationen aufzuwerten, zu betonen oder auf andere Weise angezeigte Informationen zu wiederholen. Vermitteln Sie die Informationen jedoch nicht ausschließlich über die Farbe. Benutzer, die farbenblind sind oder ein monochromes Display verwenden, benötigen Alternativen zu Farben.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Verwenden von Standardeingabe-APIs mit geräteunabhängigen Aufrufen

Geräteunabhängige Aufrufe stellen sicher, dass alle Eingabegeräte gleich behandelt werden, während Sie Hilfstechnologieprodukte mit erforderlichen Informationen über die Benutzeroberfläche bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows Automation-API](windows-automation-api-overview.md)
</dt> </dl>

 

 




