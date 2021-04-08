---
description: Dieses Thema enthält Aktionen zum Erstellen von Code, der mehrere Märkte unterstützt. Berücksichtigen Sie diese Anweisungen als Leitfaden für den Code Entwurf und als Metriken, wenn Sie die Builds auswerten.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Internationalisierungs Checkliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861912"
---
# <a name="internationalization-checklist"></a>Internationalisierungs Checkliste

Dieses Thema enthält Aktionen zum Erstellen von Code, der mehrere Märkte unterstützt. Berücksichtigen Sie diese Anweisungen als Leitfaden für den Code Entwurf und als Metriken, wenn Sie die Builds auswerten.

-   Erstellen Sie Programmspezifikationen, die von Anfang an internationale Überlegungen berücksichtigen.
    -   Entwerfen Sie Symbole und Bitmaps so, dass Sie in den Zielmärkten sinnvoll und nicht anstößig sind und keinen Text enthalten.
    -   Design Menüs und Dialogfelder, um Platz für die Texterweiterung zu belassen. Beispielsweise werden englische Zeichen folgen häufig um 40% erweitert, wenn Sie in Deutsch oder Niederländisch übersetzt werden.
    -   Verwenden Sie keine oder Kultur abhängigen Verweise in Benutzeroberflächen Elementen oder-Meldungen.
    -   Erstellen Sie Tastenkombinationen, die auf internationalen Tastaturen zugänglich sind. Vermeiden Sie z. b. die Verwendung von Interpunktions Zeichen Schlüsseln als Tastenkombinationen, da Sie nicht immer auf internationalen Tastaturen gefunden werden oder vom Benutzer leicht erstellt werden. Beispiele für Tastaturlayouts finden Sie unter [Windows-Tastaturlayouts](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Beachten Sie lokale Gesetze, die sich auf featureentwürfe auswirken, wie z. b. Anforderungen, dass Regierungseinrichtungen Software erwerben, die mehrere offizielle
    -   Entwickeln Sie Verträge von Drittanbietern, die die internationalen Benutzeroberflächen Standards und Entwurfsentscheidungen Ihrer Organisation unterstützen.
    -   Verwenden Sie konsistente Terminologie in Benutzeroberflächen Zeichenfolgen, die übersetzt werden müssen.

<!-- -->

-   Erstellen Sie Code, der unabhängig vom Gebiets Schema ist.
    -   Verketten Sie keine Zeichen folgen, um Sätze zu bilden.
    -   Verwenden Sie eine angegebene Zeichen folgen Variable nicht in mehr als einem Kontext, wie z. b. die Wiederverwendung eines Satz Fragments in verschiedenen Nachrichten und Eingabe Aufforderungen, da solche Zeichen folgen möglicherweise nicht leicht übersetzt werden.
    -   Dokumentieren Sie Zeichen folgen mithilfe von Kommentaren, um Kontext für Konvertierer bereitzustellen, und markieren Sie Zeichen folgen oder Zeichen, die nicht lokalisiert werden sollten.
    -   Verwenden Sie keine hart codierten Zeichen Konstanten, numerischen Konstanten, Bildschirm Positionen, Dateinamen oder Pfadnamen, die eine bestimmte Sprache voraussetzen.
    -   Stellen Sie die Puffer groß genug, um übersetzte Zeichen folgen aufzunehmen.
    -   Hiermit wird die Eingabe von Daten mit Formaten zugelassen, die je nach Gebiets Schema variieren, z. b. Datumsangaben, Uhrzeiten und Währungen.
    -   Verwenden Sie Papiergröße, Umschlag Größe und andere Standardwerte, die für ein bestimmtes Gebiets Schema geeignet sind.
    -   Stellen Sie sicher, dass jede Sprachausgabe Dokumente lesen kann, die von den anderen Editionen erstellt wurden.
    -   Stellen Sie ggf. Unterstützung für Gebiets Schema spezifische Hardware bereit.
    -   Konfigurieren Sie Features, die nicht für internationale Märkte gelten, als Implementierungs Optionen, die problemlos deaktiviert werden können.

<!-- -->

-   Erstellen Sie Code, der von Microsoft Windows angebotene internationale Funktionen nutzt.
    -   Verwenden Sie internationale Informationen, die vom System unterstützt werden (Unterstützung der Landessprache).
    -   Verwenden Sie Systemfunktionen für Sortierung, Fall Konvertierung und Zeichen folgen Zuordnung.
    -   Verwenden Sie generische textlayoutfunktionen.
    -   Reagieren Sie auf Änderungen an den internationalen Einstellungen in der Systemsteuerung.
    -   Behandeln Sie die "WM \_ inputlangchangerequest"-Nachricht.
    -   Unterstützung für Eingabemethoden-Editoren, vertikalen Text und Zeilenumbruch Regeln in ostasiatischen Editionen.

<!-- -->

-   Kompilieren Sie alle internationalen Editionen des Programms aus einem Satz von Quelldateien.
    -   Minimieren oder eliminieren Sie Mechanismen, die erfordern, dass Code für verschiedene sprach Editionen neu kompiliert wird.
    -   Speichern Sie lokalisierbare Elemente, z. b. Zeichen folgen und Symbole, in Windows-Ressourcen Dateien.
    -   Speichern Sie Dokumente in allen Sprach Editionen, die das gleiche Dateiformat aufweisen.

<!-- -->

-   Unterstützt unterschiedliche Zeichensätze, nicht nur die lateinische 1-Codepage, Nummer 1252.
    -   Das Programm unterstützt Netzwerkumgebungen, in denen Computerbetriebs Systeme mit unterschiedlichen Standard Codepages ausführen.
    -   Verwenden Sie getcpinfoex zum Abrufen von Lead-Byte-Bereichen für ostasiatische Codepages.
    -   Analysieren Sie Doppelbyte Zeichen in ostasiatischen –-Anwendungen, es sei denn, der Code basiert auf Unicode.
    -   Unterstützung von Unicode oder Konvertierung zwischen Unicode und der lokalen Codepage.
    -   Gehen Sie nicht davon aus, dass alle Zeichen 8-Bit oder 16-Bit sind.
    -   Verwenden Sie generische Datentypen und generische Funktionsprototypen.
    -   Verwenden Sie die Schriftart CharSet-Eigenschaft, die enumfontfamiliesex und die allgemeine Dialog Funktion "choosefont" aufruft.
    -   Sie können Text mit den Schriftarten anzeigen und drucken, die für das Gebiets Schema geeignet sind.

<!-- -->

-   Testen Sie die internationalen Features des Programms.
    -   Der übersetzte Text muss den Standards von systemeigenen Referenten entsprechen.
    -   Die Größe der Dialog Felder sollte ordnungsgemäß geändert werden, und der Text sollte bei der Anzeige unterschiedlicher Sprachen ordnungsgemäß durchgeführt werden.
    -   Dialog Felder, Status leisten, Symbolleisten und Menüs sollten auf den Bildschirm passen und lesbar lesbar sein, wenn die Anzeige in unterschiedlichen Auflösungen für alle übersetzten Sprachen festgelegt ist.
    -   Menü-und Dialogfeld-Accelerators sollten eindeutig sein.
    -   Benutzer sollten in der Lage sein, Zeichen aus nicht-europäischen Skripts in Dokumente, Dialogfelder und Dateinamen einzugeben.
    -   Benutzer sollten in der Lage sein, Zeichen aus nichteuropäischen Skripts auszuschneiden, einzufügen, zu speichern und zu drucken.
    -   Sortierung und Groß-/Kleinschreibung sollten für verschiedene Gebiets Schemas genau sein.
    -   Die Anwendung sollte in lokalisierten Editionen von Windows ordnungsgemäß funktionieren.

 

 



