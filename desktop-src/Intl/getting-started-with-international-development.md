---
description: Dieses Thema hilft Ihnen bei den ersten Schritte beim Erstellen weltweit einsatzbereiter Anwendungen, indem voraussetzungen angegeben, Technologien zusammengefasst und ein Tutorial zu den ersten Schritte eingeführt wird.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Erste Schritte mit International Windows Development
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346f03717b5f50c27911891daaea8aa4ed55ce199e7ca807690d2f3185d8114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949429"
---
# <a name="getting-started-with-international-windows-development"></a>Erste Schritte mit International Windows Development

Dieses Thema hilft Ihnen bei den ersten Schritte beim Erstellen weltweit einsatzbereiter Anwendungen, indem voraussetzungen angegeben, Technologien zusammengefasst und ein Tutorial zu den ersten Schritte eingeführt wird.

## <a name="getting-started"></a>Erste Schritte

Wenn Sie Anwendungen für Benutzer in einem einzigen Locale schreiben, können diese Anwendungen auch dann erfolgreich sein, wenn Sie sie mit lokalen Annahmen entwerfen, z. B. das Präsentieren von Datumsangaben in einem bestimmten Format oder das Sortieren von Zeichenfolgen in einer bestimmten Sequenz. Jetzt müssen Sie jedoch sicherstellen, dass Ihre Anwendungen in mehreren Ländern von Benutzern verwendet werden können, die über unterschiedliche Sprachen und Kulturen verfügen. Damit die Anwendung in mehreren Lokalen erfolgreich ausgeführt werden kann, müssen sie sich an das Von ihnen ausgeführte Locale anpassen. Diese Flexibilität ist wichtig, unabhängig davon, ob Sie sie einer vorhandenen Anwendung hinzufügen oder in eine neue Anwendung entwerfen.

Dieser Abschnitt hilft Ihnen bei den ersten Schritte in der internationalen Entwicklung. Es werden Links zu Themen angezeigt, die eine Übersicht über die Voraussetzungen für die Internationalisierung bereitstellen. Es fasst die Technologien zusammen, die das SDK für die Unterstützung von weltweiten Kunden anbietet. Schließlich enthält dieser Abschnitt eine Beispielanwendung, die ein Problem löst, das beim Schreiben von globaler Software häufig auftreten kann.

## <a name="prerequisites"></a>Voraussetzungen

Sie sollten sich mit den Problemen vertraut machen, die bei der Entwicklung von internationaler Software für Windows. Beginnen Sie mit diesen Übersichten.

-   [Grundlegendes zur Internationalisierung](understanding-internationalization.md) erklärt die zusätzlichen Schwierigkeiten bei der Entwicklung weltweit einsatzbereiter Anwendungen und definiert wichtige Begriffe.
-   Das [Thema Get World-Ready](https://msdn.microsoft.com/goglobal/bb895995.aspx) führt Sie zu Richtlinien und bewährten Methoden, die Sie bei Bedarf überspringen oder sich damit beschäftigen können.
-   Die [Prüfliste für die Internationalisierung](internationalization-checklist.md) fasst die Aktionen zusammen, die Sie ergreifen sollten, um eine weltweit einsatzbereite Anwendung zu erstellen.
-   Sicherheit ist bei der Softwareentwicklung immer ein Problem, aber Sie müssen bei der Entwicklung von internationaler Software zusätzliche Probleme berücksichtigen. Sehen Sie sich [Sicherheitsüberlegungen: Internationale Features an.](security-considerations--international-features.md)

Beachten Sie auch die umfangreicheren Artikel, die Sie im [Go Global Developer Center](https://msdn.microsoft.com/globalization/mt613165) im Abschnitt Globalisierung Schritt für [Schritt](https://msdn.microsoft.com/globalization/mt642951) finden. Wenn Sie internationale Software entwickeln, sollten Sie die zusätzlichen Übersichten und ausführlichen Artikel lesen, die Sie dort finden.

## <a name="learning-paths"></a>Lernpfade

Der Pfad, den Sie als Nächstes beim Lernen zum Erstellen von internationaler Software befolgen, hängt von den Szenarien ab, denen Sie gegenüber stehen. Die folgenden Szenarien basieren auf den Szenarien, die im Hauptabschnittsthema [Internationalization for Windows Applications (Internationalisierung für Windows Anwendungen) vorgestellt wurden.](international-support.md)

-   **Erstellen Sie Anwendungen, die in mehreren Regionen in mehreren Sprachen bereitgestellt werden können.**

    Die Herausforderung besteht darin, eine Anwendung zu entwickeln, die nicht für jede Sprache oder Kultur umgeschrieben werden muss.

    -   Lesen Sie den Artikel [Understanding mehrsprachige Benutzeroberfläche (SCHREIBGESCHÜTZT) .](./about-multilingual-user-interface.md)
    -   Sehen Sie sich die Dokumentation für [mehrsprachige Benutzeroberfläche.](multilingual-user-interface.md)
    -   Erste Schritte mit der [Anwendung Hello HELLO.](#the-hello-mui-application)

-   **Unterstützt die Eingabe und Anzeige verschiedener Sprachen, Zeichensätze und Schriftarten.**

    Ihre Anwendung muss möglicherweise mehrere Zeichensätze unterstützen, komplexe Skripts unterstützen (z. B. diejenigen, die zum Darstellen der Sprachen Hebräisch, Arabisch, Thai und Indic verwendet werden), dem Benutzer die Auswahl von internationalen Schriftarten ermöglichen oder dem Benutzer die Eingabe von Zeichen und Symbolen, z. B. japanischen Kanji, für andere Sprachen mithilfe einer Standardtastatur erlauben.

    -   Lesen Sie die folgenden Artikel:

        -   [Skript- und Schriftartunterstützung in Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Eingabesprache: Tastaturen und IMEs](https://msdn.microsoft.com/globalization/mt662332)

    -   Sehen Sie sich die Dokumentation zu folgenden Informationen an:

        -   [Unicode und Zeichensätze](unicode-and-character-sets.md)
        -   [Internationale Schriftarten und Textanzeige](international-fonts-and-text-display.md)
        -   [Eingabemethode-Manager](input-method-manager.md)

-   **Anzeigen kulturabhängiger Objekte in geeigneten Formaten.**

    Internationale Anwendungen sollten Mithilfe von Locale-Einstellungen Zeichenfolgen ordnungsgemäß sortieren und kultursensible Informationen wie Uhrzeit, Datumsangaben und Währung anzeigen.

    -   Sehen Sie sich [das Knowledge Center für den National Language Support an.](./national-language-support-reference.md)
    -   Sehen Sie sich die Dokumentation [zu National Language Support (NLS) an.](national-language-support.md)

-   **Entdecken Sie die Sprache oder das Skript, die bzw. das der Benutzer verwendet, und wenden Sie sie auf die anderen Dienste der Anwendung an.**

    Wenn Ihre Anwendung die Sprache bestimmen kann, in der Text und Benutzereingaben geschrieben werden, kann sie Inhalte wie Eingabeaufforderungen oder Hilfe in einer verständlichen Sprache anzeigen.

    -   Lesen Sie den Artikel [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).
    -   Sehen Sie sich die Dokumentation [für erweiterte linguistische Dienste (ELS) an.](extended-linguistic-services.md)

## <a name="internationalization-technologies-in-the-sdk"></a>Internationalisierungstechnologien im SDK

Der Abschnitt "International Development Support" des SDK enthält Technologien, die es der Anwendung ermöglichen, Sprachen, Lokalien und lokale Formate aufzählen zu können. Sie können sie in Microsoft Win32-Anwendungen verwenden, die Sie in C oder C++ schreiben.

Die [erweiterten linguistischen Dienste](extended-linguistic-services.md) bieten von Microsoft patentierte Technologie für die Identifizierung von Sprachen und Skripts in Text. Ihre Anwendung kann die verfügbaren Dienste anhand der Kategorie sowie der Eingabe- und Ausgabesprache, des Skripts und des Inhaltstyps bestimmen.

[International Fonts and Text Display](international-fonts-and-text-display.md) bietet Informationen zu internationalen Schriftarten, komplexen Skripts und Glyphen sowie zum feinen Rendering der Typografie auf der Windows Plattform.

[Input Method Manager (IMM)](input-method-manager.md) ist eine Technologie, die der Anwendung hilft, Eingaben von der IME-Software (Input Method Editor) zu empfangen, die wiederum das Eingeben von Zeichen und Symbolen, z. B. japanischem Kanji, für andere Sprachen mithilfe einer Standardtastatur ermöglicht.

## <a name="the-hello-mui-application"></a>Die Hello HELLO-Anwendung

Eine häufige Aufgabe in der internationalen Entwicklung beginnt mit einer einsprachigen Anwendung, die Sie weltweit bereit machen müssen. Sie müssen Unterstützung für zusätzliche Sprachen hinzufügen, aber auf eine Weise, die es nicht erfordert, dass Sie den Code für jede neue Sprache oder Kultur neu schreiben.

Diese Aufgabe bietet die Möglichkeit, ein Tutorial zu präsentieren, in dem Sie schritt für Schritt durch die Erstellung einer Hello TUTORIALS-Anwendung geführt werden. Dabei werden das [mehrsprachige Benutzeroberfläche-Ressourcenmodell (MEHRSPRACHIGE BENUTZEROBERFLÄCHE)](multilingual-user-interface.md) und die zugehörige Unterstützung in Windows.

In diesem Tutorial wird das Konzept der vertrauten Anwendung Hallo Welt und die Verwendung von TUTORIALS zum Erstellen einer einfachen mehrsprachigen Anwendung demonstriert.

Sie können das Tutorial Hello TUTORIALS unter Adding mehrsprachige Benutzeroberfläche Support to an Application (Hinzufügen von Support [zu einer Anwendung) beginnen.](creating-a-multilingual-user-interface-application.md)

 

 
