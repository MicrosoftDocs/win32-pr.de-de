---
description: In diesem Abschnitt werden die Technologien in Windows beschrieben, mit denen Sie die vielen Kulturen und geschriebenen Sprachen des internationalen Marketplace in Ihrer C- oder C++-basierten Microsoft Win32-Anwendung unterstützen können.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internationalisierung für Windows-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78f4831390ffc31a5f3290f0784d32c3aa1044863c708e6e0329225519c2cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147543"
---
# <a name="internationalization-for-windows-applications"></a>Internationalisierung für Windows-Anwendungen

(früher als "International Support" bezeichnet)

In diesem Abschnitt werden die Technologien in Windows beschrieben, mit denen Sie die vielen Kulturen und geschriebenen Sprachen des internationalen Marketplace in Ihrer C- oder C++-basierten Microsoft Win32-Anwendung unterstützen können.

Windows ist zu einer wichtigen Plattform für Kunden weltweit geworden. Internationale Benutzer erwarten Lösungen, die an ihre Sprachen und Regionen auf der ganzen Welt angepasst sind. In diesem Abschnitt finden Sie die Informationen, die Sie zum Entwickeln von Lösungen mit mehreren Sprachen, Nehmern und mehreren Standorts benötigen. Dank der in Windows integrierten internationalen Unterstützung können Sie viele Szenarien mit weniger Engineeringaufwand als je zuvor implementieren.

Die Entwicklung weltweit einsatzbereiter Anwendungen erfordert die Verwendung vieler Dienste und Tools. Windows enthält Features, mit denen Sie Lösungen entwickeln können, die:

- Unterstützen Sie die verschiedenen sprach- und ortsspezifischen Anforderungen von Benutzern auf der ganzen Welt (einschließlich spezieller Textunterstützung, Sortierverhalten, Datums- und Uhrzeitformatierung und Tastaturlayouts). (Weitere Informationen finden Sie unter [National Language Support Knowledge Center](./national-language-support-reference.md).)
- Sie sind globalisiert (können weltweit aus einem einzelnen Binärbild bereitgestellt werden) und können lokalisiert werden (können für bestimmte lokale Märkte angepasst werden). (Weitere Informationen finden Sie unter [mehrsprachige Benutzeroberfläche](./multilingual-user-interface.md).)
- Zeigen Sie internationale Schriftarten und Text an, und erlauben Sie Benutzern, die schriftart anzugeben, die sie möchten. (Weitere Informationen finden Sie unter [Skript- und Schriftartunterstützung in Windows](/globalization/input/font-support).)
- Erlauben Sie dem Benutzer, komplexe Zeichen und Symbole mit einer Standardtastatur eineingaben.
- Bieten Unterstützung für viele verschiedene geschriebene Sprachen durch Unicode und herkömmliche Zeichensätze.
- Entdecken Sie die Spracheingabe durch einen Benutzer, und passen Sie die von Ihrer Anwendung bereitgestellte Benutzererfahrung an. (Weitere Informationen finden Sie unter [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).)

## <a name="in-this-section"></a>In diesem Abschnitt

Die folgenden internationalen Supporttechnologien sind in diesem Abschnitt dokumentiert. Sie werden mit einigen wichtigen Szenarien aufgelistet, für die sie verwendet werden können.

- [Erste Schritte mit International Windows Development](getting-started-with-international-development.md)

    Beschreibt die ersten Schritte beim Erstellen weltweit einsatzbereiter Anwendungen und enthält ein Tutorial, das eine allgemeine Aufgabe beim Schreiben von globaler Software veranschaulicht.

    Häufige Szenarien:

    - Bestimmen Sie einen Weg, um zu lernen, wie internationale Software entwickelt werden kann.
    - Entdecken Sie die Internationalisierungstechnologien, die im Microsoft Windows Software Development Kit (SDK) verfügbar sind.
    - Führen Sie ein Tutorial aus, in dem eine vorhandene einsprachliche Anwendung verwendet und Unterstützung für weitere Sprachen unterstützt wird.

- [Globalisierungsdienste](globalization-services.md)

    Beschreibt erweiterte linguistische Dienste [(Extended Linguistic Services, ELS),](extended-linguistic-services.md)mit denen Sie die Sprache, in der Text- und Benutzereingaben geschrieben werden, und die Unterstützung der nationalen Sprache [(National Language Support, NLS)](national-language-support.md)entdecken können, wodurch eine Anwendung Mithilfe von Locale-Informationen kultursensible Informationen (z. B. Uhrzeit, Datumsangaben und Währung) anzeigen und Zeichenfolgen ordnungsgemäß sortieren kann.

    Häufige Szenarien:

    - Entdecken Sie die Sprache der Benutzereingabe, damit Hilfeinhalte in einer verständlichen Sprache angezeigt werden können.
    - Entdecken Sie das Skript, das in text verwendet wird, der angezeigt werden soll. Wenn es sich um vereinfachtes oder traditionelles Chinesisch handelt, bieten Sie dem Benutzer die Möglichkeit, den Text von einem zum anderen transliteriert zu lassen.
    - Erlauben Sie dem Benutzer, ein Lokales (eine Sammlung sprachbezogener Benutzerpräferenzinformationen) auszuwählen.
    - Anzeigen von Zeiten, Datumsangaben, Kalenderinformationen, Währungen und vielen anderen kulturabhängigen Objekten in geeigneten Sprachen und Formaten.
    - Sortieren Sie Zeichenfolgen in der Reihenfolge, die vom Benutzer eines bestimmten Locales erwartet wird.

- [Eingabemethode-Manager](input-method-manager.md)

    Beschreibt die Technologie, die von einer Anwendung für die Kommunikation mit einem Eingabemethode-Editor (IME) verwendet wird. Mit dem IME können Computerbenutzer komplexe Zeichen und Symbole mithilfe einer Standardtastatur eingeben.

    Allgemeines Szenario:

    - Erlauben Sie dem Benutzer die Verwendung einer Standardtastatur, um japanische Kanjizeichen eineingaben zu können.

- [Internationale Schriftarten und Textanzeige](international-fonts-and-text-display.md)

    Beschreibt die Unterstützung, die von der Windows-Plattform für internationale Schriftarten, internationalen Text und feinen Typografie bereitgestellt wird.

    Häufige Szenarien:

    - Ermöglicht es dem Benutzer, internationale Schriftarten basierend auf dem Zeichensatz auszuwählen.
    - Internationalen Text anzeigen.
    - Verarbeiten komplexer Skripts, einschließlich bidirektionalem Rendering, kontextbezogener Formung und Ligaturen (Uniscribe).
    - Lassen Sie ein hohes Maß an Kontrolle für die Feintypografie (Uniscribe) zu.

- [Multilingual User Interface](multilingual-user-interface.md)

    Beschreibt, wie Anwendungen sprachabhängige Ressourcen von sprachneutralem Code für unterstützte Benutzeroberflächensprachen trennen können.

    Häufige Szenarien:

    - Erstellen Sie regionale oder weltweite Images für eine einzelne Bereitstellung einer Anwendung.
    - Lokalisieren Sie eine Lösung, indem Sie Anwendungsressourcen ohne Änderungen am Quellcode der Anwendung aktualisieren.
    - Ermöglicht Benutzern, zur Laufzeit von einer Benutzeroberflächensprache in eine andere zu wechseln.

- [Unicode und Zeichensätze](unicode-and-character-sets.md)

    Beschreibt, wie Anwendungen Unicode nutzen können, den weltweiten Zeichencodierungsstandard, der 16-Bit-Codewerte verwendet, um alle zeichen, die im modernen Computing verwendet werden, einschließlich technischer Symbole und Sonderzeichen, die bei der Veröffentlichung verwendet werden, darstellen.

    Häufige Szenarien:

    - Unterstützen Sie die vielen verschiedenen Sprachen des internationalen Marketplace über Unicode.
    - Konvertieren Sie Unicode-Zeichen bei Bedarf in und aus anderen Zeichensätzen.

- [Sicherheitsüberlegungen: Internationale Features](security-considerations--international-features.md)

    Enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit internationalen Entwicklungsunterstützungsfeatures.

    Die Sicherheitsinformationen beziehen sich auf alle Szenarien.

## <a name="related-international-technologies"></a>Verwandte internationale Technologien

Internationale Entwicklungsunterstützung ist auch für Anwendungen verfügbar, die in verwaltetem Code geschrieben sind. Wenn Sie für die .NET Framework entwickeln, benötigen Sie einige oder alle dieser Schritte:

- Der [System.Globalization-Namespace enthält](/dotnet/api/system.globalization) Klassen, die kulturbezogene Informationen definieren und erweiterte Globalisierungsfunktionen bereitstellen.
- Der [System.Text-Namespace enthält](/dotnet/api/system.text) Klassen, die Zeichencodierungen darstellen, Zeichenblöcke konvertieren sowie Zeichenfolgenobjekte bearbeiten und formatieren.
