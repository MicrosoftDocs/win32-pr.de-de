---
title: Bewährte Methoden für Eingabehilfen
description: Die Implementierung der in diesem Abschnitt beschriebenen bewährten Methoden hilft sicherzustellen, dass Ihre Anwendung für Personen zugänglich ist, die Hilfstechnologieprodukte verwenden.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f596378c55b5f99af5b24fa60a23d980407392298fe2ad656579730fbab709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327870"
---
# <a name="accessibility-best-practices"></a>Bewährte Methoden für Eingabehilfen

Die Implementierung der in diesem Abschnitt beschriebenen bewährten Methoden hilft sicherzustellen, dass Ihre Anwendung für Personen zugänglich ist, die Hilfstechnologieprodukte verwenden. Viele dieser bewährten Methoden konzentrieren sich auf einen guten Benutzeroberflächenentwurf. Jede bewährte Methode umfasst Implementierungsinformationen für Steuerelemente oder Anwendungen. In vielen Fällen ist ein Teil der Arbeit zur Erfüllung dieser bewährten Methoden bereits in den Steuerelementen enthalten.

Dieses Thema enthält folgende Abschnitte:

-   [Programmgesteuerter Zugriff](#programmatic-access)
    -   [Aktivieren des programmgesteuerten Zugriffs auf alle Elemente der Benutzeroberfläche und auf Text](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Platzieren von Namen, Titeln und Beschreibungen auf Benutzeroberflächenobjekte, Frames und Seiten](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Gewährleisten der Auslösung programmgesteuerter Ereignisse durch alle Aktivitäten auf der Benutzeroberfläche](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Benutzer Einstellungen](#user-settings)
    -   [Respektieren aller systemweiten Einstellungen und Beachten der Barrierefreiheitsfunktionen](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Entwurf der visuellen Benutzeroberfläche](#visual-ui-design)
    -   [Farben nicht Hard-Code](#do-not-hard-code-colors)
    -   [Unterstützen von hohem Kontrast und allen Systemanzeigeattributen](#support-high-contrast-and-all-system-display-attributes)
    -   [Gewährleisten der ordnungsgemäßen Skalierung aller Benutzeroberflächenelemente bei beliebiger DPI-Einstellung](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Tastaturnavigation](#keyboard-navigation)
    -   [Bereitstellen einer Tastaturschnittstelle für alle Elemente der Benutzeroberfläche](#provide-keyboard-interface-for-all-ui-elements)
    -   [Anzeigen des Tastaturfokus](#show-the-keyboard-focus)
    -   [Unterstützen von Navigationsstandards und leistungsstarken Navigationsschemas](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Vermeiden störender Auswirkungen der Mausposition auf die Tastaturnavigation](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Multi-modale Schnittstelle](#multi-modal-interface)
    -   [Bereitstellen von auswählbaren Entsprechungen für Nicht-Text-Elemente](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Verwenden von Farbe und Bereitstellen von Alternativen für Farbe](#use-color-but-also-provide-alternatives-to-color)
    -   [Verwenden von Standardeingabe-APIs mit geräteunabhängigen Aufrufen](#use-standard-input-apis-with-device-independent-calls)
-   [Zugehörige Themen](#related-topics)

## <a name="programmatic-access"></a>Programmgesteuerter Zugriff

Die bewährten Methoden in diesem Abschnitt stellen sicher, dass Hilfstechnologieprodukte über einen angemessenen programmgesteuerten Zugriff auf Benutzeroberflächeninformationen und -funktionen verfügen.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Aktivieren des programmgesteuerten Zugriffs auf alle Elemente der Benutzeroberfläche und auf Text

Die Benutzeroberflächenelemente Ihrer Anwendung müssen programmgesteuert für Hilfstechnologieprodukte zugänglich sein. Alle Benutzeroberflächenelemente müssen Bezeichnungen haben, sie müssen alle Eigenschaftswerte verfügbar machen und alle entsprechenden Ereignisse aussetzen. Bei den Windows-Standardsteuerelementen erfolgt der Großteil dieser Arbeit bereits über die Microsoft Benutzeroberflächenautomatisierung und Microsoft Active Accessibility Proxyobjekte. Benutzerdefinierte Steuerelemente erfordern jedoch zusätzliche Arbeit, um sicherzustellen, dass sie vollständig verfügbar gemacht werden, damit Hilfstechnologieanbieter Elemente ihrer Anwendungsbenutzeroberfläche identifizieren und bearbeiten können.

Wenn Sie diese bewährte Methode verwenden, können Hilfstechnologieanbieter Elemente der Benutzeroberfläche Ihres Produkts identifizieren und bearbeiten.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Platzieren von Namen, Titeln und Beschreibungen auf Benutzeroberflächenobjekte, Frames und Seiten

Da Hilfstechnologieprodukte – insbesondere Sprachlesegeräte – Titel verwenden, um die Position eines Frames, Objekts oder einer Seite im Navigationsschema zu verstehen, müssen die Titel sehr beschreibend sein. Gute beschreibende Titel ermöglichen es Hilfstechnologieprodukten, Benutzeroberflächenelemente in Steuerelementen und Anwendungen zu identifizieren und zu bearbeiten. Beispielsweise ist ein Webseitentitel "Microsoft-Webseite" nicht von Nutzen, wenn der Benutzer tief in einen bestimmten Bereich navigiert ist. Ein beschreibender Titel ist entscheidend für Benutzer, die blind sind und von Sprachbildschirmen abhängig sind.

Mithilfe dieser bewährten Methode können Hilfstechnologieprodukte die Benutzeroberfläche in Beispielsteuerelementen und -anwendungen identifizieren und bearbeiten.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Gewährleisten der Auslösung programmgesteuerter Ereignisse durch alle Aktivitäten auf der Benutzeroberfläche

Ihre Anwendung sollte Immer dann Ereignisse aus-,wenn Änderungen am Zustand oder der Darstellung eines Benutzeroberflächenelements auftreten.

Nach dieser bewährten Methode können Hilfstechnologieprodukte auf Änderungen in der Benutzeroberfläche lauschen und den Benutzer über diese Änderungen benachrichtigen.

## <a name="user-settings"></a>Benutzereinstellungen

Die bewährte Methode in diesem Abschnitt stellt sicher, dass Steuerelemente oder Anwendungen die Benutzereinstellungen nicht außer Kraft setzen.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respektieren aller systemweiten Einstellungen und Beachten der Barrierefreiheitsfunktionen

Benutzer können Systemsteuerung verwenden, um einige systemweite Flags zu setzen. Andere Flags können programmgesteuert festgelegt werden. Diese Einstellungen dürfen nicht von Steuerelementen oder Anwendungen geändert werden. Darüber hinaus müssen Anwendungen die Einstellungen für die Barrierefreiheit ihres Hostbetriebssystems unterstützen.

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

Stellen Sie sicher, dass alle Benutzeroberflächenelemente ordnungsgemäß um eine beliebige dpi-Einstellung (Dots per Inch) skaliert werden können. Stellen Sie außerdem sicher, dass Benutzeroberflächenelemente in einen Bildschirm von 1.024 x 768 mit 120 DPI-Punkten (Dots per Inch) passen.

## <a name="keyboard-navigation"></a>Tastaturnavigation

Die bewährten Methoden in diesem Abschnitt stellen sicher, dass alle Anwendungsfunktionen für Benutzer zugänglich sind, die sich auf die Tastatur verlassen.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Bereitstellen einer Tastaturschnittstelle für alle Elemente der Benutzeroberfläche

Tabstopps, insbesondere bei sorgfältiger Planung, bieten Benutzern eine andere Möglichkeit, in der Benutzeroberfläche zu navigieren.

Anwendungen sollten die folgenden Tastaturschnittstellen bereitstellen:

-   Tabstopps für alle Steuerelemente, mit denen der Benutzer interagieren kann, z. B. Schaltflächen, Links oder Listenfelder.
-   Logische Registerkartenfolge.

### <a name="show-the-keyboard-focus"></a>Anzeigen des Tastaturfokus

Benutzer müssen wissen, welches Objekt den Tastaturfokus hat, damit sie die Auswirkungen ihrer Tastatureingaben voraussehen können. Verwenden Sie Farben, Schriftarten oder grafische Darstellungen (z. B. Rechtecke oder eine Vergrößerung), um den Tastaturfokus hervorzuheben. Um den Tastaturfokus akustisch hervorzuheben, ändern Sie die Lautstärke, Tonhöhe oder Tonqualität.

Um Verwechselungen zu vermeiden, sollten Anwendungen alle visuellen Fokusindikatoren ausblenden und die Auswahl abblenden, die sich in inaktiven Fenstern (oder Bereichen) befindet.

Anwendungen sollten beim Tastaturfokus wie folgt vorgehen:

-   Ein Element sollte immer den Tastaturfokus haben.
-   Der Tastaturfokus sollte sichtbar und offensichtlich sein.
-   Auswahlen und/oder fokussierte Elemente sollten visuell hervorgehoben werden.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Unterstützen von Navigationsstandards und leistungsstarken Navigationsschemas

Verschiedene Aspekte der Tastaturnavigation bieten Benutzern verschiedene Möglichkeiten, auf der Benutzeroberfläche zu navigieren.

Anwendungen sollten die folgenden Tastaturschnittstellen bereitstellen:

-   Tastenkombinationen und unterstrichene Zugriffsschlüssel für alle Befehle, Menüs und Steuerelemente.
-   Tastenkombinationen zu wichtigen Links.
-   Alle Menüelemente verfügen über einen Zugriffsschlüssel. Alle Schaltflächen verfügen über Zugriffstasten, alle Befehle verfügen über eine Zugriffstaste.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Vermeiden störender Auswirkungen der Mausposition auf die Tastaturnavigation

Die Position des Mauszeigers sollte nicht die Tastaturnavigation behindern. Wenn sich der Mauszeiger z. B. an einer beliebigen Position befindet und der Benutzer über die Tastatur navigiert, darf ein Mausklick nur auftreten, wenn er vom Benutzer initiiert wird.

## <a name="multi-modal-interface"></a>Multi-modale Schnittstelle

Die bewährte Methode in diesem Abschnitt stellt sicher, dass die Benutzeroberfläche der Anwendung Alternativen für visuelle Elemente enthält.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Bereitstellen von auswählbaren Entsprechungen für Nicht-Text-Elemente

Geben Sie für jedes Nicht-Textelement eine vom Benutzer auswählbare Entsprechung für Text, Aufzeichnungen oder Audiobeschreibungen ein, z. B. alternativen Text, Beschriftungen oder visuelles Feedback.

Nicht-Text-Elemente decken eine Vielzahl von Benutzeroberflächenelementen ab, einschließlich Bildern, Bildzuordnungsregionen, Animationen, Applets, Frames, Skripts, grafischen Schaltflächen, Sounds, eigenständigen Audiodateien und Videos. Nicht-Text-Elemente sind wichtig, wenn sie visuelle Informationen, Sprache oder allgemeine Audioinformationen enthalten, auf die der Benutzer Zugriff benötigt, um den Inhalt der Benutzeroberfläche zu verstehen.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Verwenden von Farbe und Bereitstellen von Alternativen für Farbe

Verwenden Sie Farbe, um Informationen aufzuwerten, zu betonen oder auf andere Weise angezeigte Informationen zu wiederholen. Vermitteln Sie die Informationen jedoch nicht ausschließlich über die Farbe. Benutzer, die farbenblind sind oder ein monochromes Display verwenden, benötigen Alternativen zu Farben.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Verwenden von Standardeingabe-APIs mit geräteunabhängigen Aufrufen

Geräteunabhängige Aufrufe stellen sicher, dass alle Eingabegeräte gleich behandelt werden, und stellen gleichzeitig Hilfstechnologieprodukte mit erforderlichen Informationen über die Benutzeroberfläche bereit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Übersicht über die Automatisierungs-API](windows-automation-api-overview.md)
</dt> </dl>

 

 




