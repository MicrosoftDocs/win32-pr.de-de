---
description: In diesem Abschnitt werden die Technologien in Windows beschrieben, mit denen Sie die vielen Kulturen und geschriebenen Sprachen des internationalen Marketplace in Ihrer C-oder C++ basierten Microsoft Win32-Anwendung unterstützen können.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internationalisierung für Windows-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f6e4952c94af3b14dc0e8f4f135c1cc0cebafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752336"
---
# <a name="internationalization-for-windows-applications"></a>Internationalisierung für Windows-Anwendungen

(Früher mit dem Titel "internationale Unterstützung")

In diesem Abschnitt werden die Technologien in Windows beschrieben, mit denen Sie die vielen Kulturen und geschriebenen Sprachen des internationalen Marketplace in Ihrer C-oder C++ basierten Microsoft Win32-Anwendung unterstützen können.

Windows ist eine wichtige Plattform für Kunden auf der ganzen Welt. Internationale Benutzer erwarten Lösungen, die an Ihre Sprachen und Regionen auf der ganzen Welt angepasst sind. In diesem Abschnitt finden Sie die Informationen, die Sie benötigen, um mehrsprachige, multikulturelle und Multisite-Lösungen zu entwickeln. Die in Windows integrierte internationale Unterstützung ermöglicht es Ihnen, viele Szenarien zu implementieren, bei denen weniger Entwicklungsaufwand als je zuvor vorliegt.

Die Entwicklung von weltweit einsetzbaren Anwendungen erfordert die Verwendung vieler Dienste und Tools. Windows enthält Features, mit denen Sie Lösungen entwickeln können, die Folgendes ermöglichen:

- Unterstützung der verschiedenen sprachspezifischen und Gebiets Schema spezifischen Anforderungen von Benutzern auf der ganzen Welt (einschließlich spezieller Textunterstützung, Sortier Verhalten, Datums-und Uhrzeit Formatierung und Tastaturlayouts). (Weitere Informationen finden Sie [unter National Language Support Knowledge Center](./national-language-support-reference.md).)
- Sind globalisiert (kann weltweit über ein einzelnes binäres Image bereitgestellt werden) und lokalisiert werden können (kann für bestimmte lokale Märkte angepasst werden). (Weitere Informationen finden Sie unter [mehrsprachige Benutzeroberfläche](./multilingual-user-interface.md).)
- Zeigen Sie internationale Schriftarten und Text an, und erlauben Sie Benutzern, die gewünschte Schriftart anzugeben. (Weitere Informationen finden Sie [unter Skript-und Schriftart Unterstützung in Windows](/globalization/input/font-support).)
- Ermöglicht es dem Benutzer, komplexe Zeichen und Symbole mit einer Standardtastatur einzugeben.
- Unterstützung für viele verschiedene geschriebene Sprachen mithilfe von Unicode-und herkömmlichen Zeichensätzen bereitstellen.
- Entdecken Sie die Spracheingabe durch einen Benutzer, und passen Sie die von Ihrer Anwendung bereitgestellte Benutzer Darstellung an. (Weitere Informationen finden Sie unter [Schreiben von weltweit einsatzfähigen Anwendungen in Windows: Erweiterte linguistische Dienste in Windows](./using-extended-linguistic-services.md).)

## <a name="in-this-section"></a>In diesem Abschnitt

Die folgenden internationalen Support Technologien sind in diesem Abschnitt dokumentiert. Sie werden mit einigen wichtigen Szenarien aufgelistet, für die Sie verwendet werden können.

- [Einstieg in die internationale Windows-Entwicklung](getting-started-with-international-development.md)

    Beschreibt die ersten Schritte beim Erstellen von weltweit einsatzfähigen Anwendungen und bietet ein Tutorial, das eine gängige Aufgabe beim Schreiben von globaler Software veranschaulicht.

    Häufige Szenarien:

    - Legen Sie einen Weg fest, um zu erfahren, wie Sie internationale Software entwickeln.
    - Entdecken Sie die im Microsoft Windows Software Development Kit (SDK) verfügbaren Internationalisierungs Technologien.
    - Befolgen Sie ein Tutorial, das eine vorhandene monolinguale Anwendung annimmt und Unterstützung für zusätzliche Sprachen hinzufügt.

- [Globalisierungs Dienste](globalization-services.md)

    Beschreibt die [erweiterten linguistischen Dienste](extended-linguistic-services.md), mit denen Sie die Sprache, in der Text-und Benutzereingaben geschrieben werden, und die [Unterstützung der Landessprache (NLS)](national-language-support.md)ermitteln können, mit der eine Anwendung Gebiets Schema Informationen zum Anzeigen Kultur bezogener Informationen (z. b. Zeit, Datumsangaben und Währungen) sowie zum ordnungsgemäßen Sortieren von Zeichen folgen verwenden kann.

    Häufige Szenarien:

    - Entdecken Sie die Sprache der Benutzereingaben, damit Hilfe Inhalte in einer verständlichen Sprache angezeigt werden können.
    - Erkennen Sie das Skript, das in Text verwendet wird, der angezeigt werden soll. Wenn Sie vereinfacht oder Chinesisch (traditionell) ist, bieten Sie dem Benutzer die Möglichkeit, den Text von einem zum anderen zu übertragen.
    - Ermöglicht dem Benutzer die Auswahl eines Gebiets Schemas (eine Sammlung von sprachbezogenen Benutzer Einstellungs Informationen).
    - Anzeige Zeiten, Datumsangaben, Kalenderinformationen, Währungen und viele andere Kultur abhängige Objekte in den entsprechenden Sprachen und Formaten.
    - Sortiert Zeichen folgen in die Reihenfolge, die vom Benutzer eines bestimmten Gebiets Schemas erwartet wird.

- [Eingabemethoden-Manager](input-method-manager.md)

    Beschreibt die Technologie, die von einer Anwendung für die Kommunikation mit einem Eingabemethoden-Editor (IME) verwendet wird. Mit dem IME können Computerbenutzer komplexe Zeichen und Symbole mithilfe einer Standardtastatur eingeben.

    Gängiges Szenario:

    - Ermöglicht es dem Benutzer, eine Standardtastatur für die Eingabe japanischer Kanji-Zeichen zu verwenden.

- [Internationale Schriftarten und Text Anzeige](international-fonts-and-text-display.md)

    Beschreibt die Unterstützung, die von der Windows-Plattform für Internationale Schriftarten, internationalen Text und feine Typografie bereitgestellt wird.

    Häufige Szenarien:

    - Ermöglicht dem Benutzer die Auswahl internationaler Schriftarten basierend auf dem Zeichensatz.
    - Anzeigen von internationalem Text.
    - Verarbeiten komplexer Skripts, einschließlich bidirektionalem Rendering, Kontext Bildung und Ligaturen (unischreiber).
    - Ermöglicht ein hohes Maß an Kontrolle für die fein Typografie (unischreiber).

- [Multilingual User Interface](multilingual-user-interface.md)

    Beschreibt, wie Anwendungen sprachabhängige Ressourcen von sprach neutralem Code für unterstützte Benutzeroberflächen Sprachen trennen können.

    Häufige Szenarien:

    - Erstellen Sie regionale oder weltweite einzelne Bereitstellungs Images einer Anwendung.
    - Lokalisieren einer Lösung durch Aktualisieren von Anwendungs Ressourcen ohne Änderung des Anwendungs Quellcodes.
    - Ermöglicht es Benutzern, zur Laufzeit von einer Benutzeroberflächen Sprache zu einer anderen zu wechseln.

- [Unicode und Zeichensätze](unicode-and-character-sets.md)

    Beschreibt, wie Anwendungen Unicode nutzen können, den weltweiten Zeichen Codierungsstandard, der 16-Bit-Codewerte verwendet, um alle in modernen Computing verwendeten Zeichen darzustellen, einschließlich technischer Symbole und Sonderzeichen, die bei der Veröffentlichung verwendet werden.

    Häufige Szenarien:

    - Unterstützen Sie die vielen verschiedenen Sprachen des internationalen Marketplace über Unicode.
    - Konvertieren von Unicode-Zeichen in und aus anderen Zeichensätzen, falls erforderlich.

- [Überlegungen zur Sicherheit: Internationale Features](security-considerations--international-features.md)

    Bietet Informationen zu Sicherheitsüberlegungen im Zusammenhang mit internationalen Entwicklungs Support Features.

    Die Sicherheitsinformationen beziehen sich auf alle Szenarien.

## <a name="related-international-technologies"></a>Verwandte internationale Technologien

Internationale Entwicklungsunterstützung steht auch für in verwaltetem Code geschriebene Anwendungen zur Verfügung. Wenn Sie für die .NET Framework entwickeln, benötigen Sie einige oder alle der folgenden:

- Der [System. Globalization-Namespace](/dotnet/api/system.globalization) enthält Klassen, die kulturbezogene Informationen definieren und erweiterte Globalisierungs Funktionen bereitstellen.
- Der [System. Text-Namespace](/dotnet/api/system.text) enthält Klassen, die Zeichen Codierungen darstellen, Zeichenblöcke konvertieren und Zeichen folgen Objekte bearbeiten und formatieren.
