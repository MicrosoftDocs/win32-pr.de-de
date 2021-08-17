---
description: Dieses Thema enthält Aktionen zum Erstellen von Code, der mehrere Märkte unterstützt. Betrachten Sie diese Anweisungen als Leitfaden beim Codeentwurf und als Metriken, wenn Sie die Builds auswerten.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Prüfliste für die Internationalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4650f7bd1111f35c911d6efe12bfbec4b537f2cdabdc50160965b5e602708b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147513"
---
# <a name="internationalization-checklist"></a>Prüfliste für die Internationalisierung

Dieses Thema enthält Aktionen zum Erstellen von Code, der mehrere Märkte unterstützt. Betrachten Sie diese Anweisungen als Leitfaden beim Codeentwurf und als Metriken, wenn Sie die Builds auswerten.

-   Erstellen Sie Programmspezifikationen, die von Anfang an internationale Überlegungen berücksichtigen.
    -   Entwerfen Sie Symbole und Bitmaps so, dass sie in Ihren Zielmarkten aussagekräftig und nicht anstößig sind und keinen Text enthalten.
    -   Entwerfen Sie Menüs und Dialogfelder, um Platz für die Texterweiterung zu lassen. Beispielsweise werden englische Zeichenfolgen häufig um 40 % erweitert, wenn sie ins Deutsche oder Niederländisch übersetzt werden.
    -   Verwenden Sie keine Slang- oder kulturspezifischen Verweise in Benutzeroberflächenelementen oder Meldungen.
    -   Erstellen Sie Tastenkombinationen, auf die auf internationalen Tastaturen zugegriffen werden kann. Vermeiden Sie beispielsweise die Verwendung von Interpunktionszeichentasten als Tastenkombinationen, da sie nicht immer auf internationalen Tastaturen zu finden sind oder einfach vom Benutzer erzeugt werden. Beispiele für Tastaturlayouts finden Sie unter [Windows Tastaturlayouts](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Berücksichtigen Sie lokale Gesetze, die sich auf Featureentwürfe ausdruppen, z. B. Anforderungen, die Behörden an Software erwerben, die mehrere offizielle Sprachen unterstützt.
    -   Entwickeln Sie Drittanbietervereinbarungen, die die internationalen Ui-Standards und Entwurfsentscheidungen Ihrer Organisation unterstützen.
    -   Verwenden Sie konsistente Terminologie in Zeichenfolgen der Benutzeroberfläche, die übersetzt werden müssen.

<!-- -->

-   Erstellen Sie Code, der unabhängig vom -Locale ist.
    -   Verketten Sie keine Zeichenfolgen, um Sätze zu bilden.
    -   Verwenden Sie eine bestimmte Zeichenfolgenvariable nicht in mehr als einem Kontext, z. B. die Wiederverwendung eines Satzfragments in verschiedenen Nachrichten und Eingabeaufforderungen, da solche Zeichenfolgen möglicherweise nicht einfach zu übersetzen sind.
    -   Dokumentieren Sie Zeichenfolgen, die Kommentare verwenden, um Kontext für Translators zu bieten, und markieren Sie Zeichenfolgen oder Zeichen, die nicht lokalisiert werden sollen.
    -   Verwenden Sie keine hart codierten Zeichenkonstten, numerischen Konstanten, Bildschirmpositionen, Dateinamen oder Pfadnamen, die eine bestimmte Sprache voraussetzen.
    -   Sorgen Sie dafür, dass Puffer groß genug sind, um übersetzte Zeichenfolgen zu enthalten.
    -   Lassen Sie die Eingabe von Daten mit Formaten zu, die je nach Locale variieren, z. B. Datumsangaben, Zeiten und Währungen.
    -   Verwenden Sie Papiergröße, Umschlaggröße und andere Standardwerte, die für ein bestimmtes Locale geeignet sind.
    -   Stellen Sie sicher, dass jede Sprachedition Dokumente lesen kann, die von den anderen Editionen erstellt wurden.
    -   Stellen Sie bei Bedarf Unterstützung für die lokale Hardware zur Verfügung.
    -   Konfigurieren Sie Features, die nicht für internationale Märkte gelten, als Implementierungsoptionen, die problemlos deaktiviert werden können.

<!-- -->

-   Erstellen Sie Code, der die internationalen Funktionen von Microsoft Windows.
    -   Verwenden Sie vom System enthaltene internationale Informationen (Unterstützung der Landessprache).
    -   Verwenden Sie Systemfunktionen für Sortierung, Fallkonvertierung und Zeichenfolgenzuordnung.
    -   Verwenden Sie generische Textlayoutfunktionen.
    -   Reagieren Sie auf Änderungen an internationalen Einstellungen in Systemsteuerung.
    -   Behandeln Sie die WM \_ INPUTLANGCHANGEREQUEST-Nachricht.
    -   Unterstützung von Eingabemethode-Editoren, vertikalem Text und Zeilenumbruchregeln in ostasiatischen Editionen.

<!-- -->

-   Kompilieren Sie alle internationalen Editionen des Programms aus einem Satz von Quelldateien.
    -   Minimieren oder beseitigen Sie Mechanismen, die erfordern, dass Code für verschiedene Spracheditionen neu kompiliert wird.
    -   Store lokalisierbare Elemente, z. B. Zeichenfolgen und Symbole, in Windows Ressourcendateien.
    -   Store dokumente in allen Spracheditionen mit demselben Dateiformat.

<!-- -->

-   Unterstützung verschiedener Zeichensätze, nicht nur der lateinischen 1-Codepage, Nummer 1252.
    -   Das Programm unterstützt Netzwerkumgebungen, in denen Computer Betriebssysteme mit unterschiedlichen Standardcodepages ausführen.
    -   Verwenden Sie GetCPInfoEx, um Lead-Byte-Bereiche für ostasiatische Codepages abzurufen.
    -   Analysieren von Doppel bytezeichen in ostasiatischen Anwendungen, es sei denn, der Code basiert auf Unicode.
    -   Unterstützung von Unicode oder Konvertierung zwischen Unicode und der lokalen Codepage.
    -   Gehen Sie nicht davon aus, dass alle Zeichen 8-Bit- oder 16-Bit-Zeichen sind.
    -   Verwenden Sie generische Datentypen und generische Funktionsprototypen.
    -   Verwenden Sie die charset-Eigenschaft der Schriftart, die EnumFontFamiliesEx und die allgemeine Dialogfunktion ChooseFont aufruft.
    -   Anzeigen und Drucken von Text mit den schriftarten, die für das -Locale geeignet sind.

<!-- -->

-   Testen Sie die internationalen Features des Programms.
    -   Übersetzter Text sollte den Standards nativer Sprecher entsprechen.
    -   Die Größe der Dialogfelder sollte ordnungsgemäß geändert werden, und Text sollte entsprechend bindestrichiert werden, wenn verschiedene Sprachen angezeigt werden.
    -   Dialogfelder, Statusleisten, Symbolleisten und Menüs sollten auf den Bildschirm passen und lesbar sein, wenn die Anzeige für alle übersetzten Sprachen mit unterschiedlichen Auflösungen festgelegt ist.
    -   Die Zugriffstasten für Menüs und Dialogfelder sollten eindeutig sein.
    -   Benutzer sollten Zeichen aus nicht europäischen Skripts in Dokumente, Dialogfelder und Dateinamen eingeben können.
    -   Benutzer sollten zeichen aus nicht europäischen Skripts erfolgreich ausschneiden, einfügen, speichern und drucken können.
    -   Sortierung und Fallkonvertierung sollten für unterschiedliche Locales genau sein.
    -   Die Anwendung sollte ordnungsgemäß in lokalisierten Editionen von Windows.

 

 



