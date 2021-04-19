---
description: In diesem Thema erfahren Sie, wie Sie erstklassige Anwendungen erstellen, indem Sie Voraussetzungen angeben, Technologien zusammenfassen und ein Tutorial zu den ersten Schritten durchführen.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Einstieg in die internationale Windows-Entwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350337"
---
# <a name="getting-started-with-international-windows-development"></a>Einstieg in die internationale Windows-Entwicklung

In diesem Thema erfahren Sie, wie Sie erstklassige Anwendungen erstellen, indem Sie Voraussetzungen angeben, Technologien zusammenfassen und ein Tutorial zu den ersten Schritten durchführen.

## <a name="getting-started"></a>Erste Schritte

Wenn Sie Anwendungen für Benutzer in einem einzelnen Gebiets Schema schreiben, können diese Anwendungen auch dann erfolgreich sein, wenn Sie Sie mit Gebiets Schema spezifischen Annahmen entwerfen, wie z. b. das darstellen von Datumsangaben in einem bestimmten Format oder das Sortieren von Zeichen folgen in einer bestimmten Reihenfolge. Jetzt müssen Sie jedoch sicherstellen, dass Ihre Anwendungen in mehreren Ländern, von Benutzern mit unterschiedlichen Sprachen und unterschiedlichen Kulturen verwendet werden können. Um in mehreren Gebiets Schemas erfolgreich zu sein, müssen die Anwendungen an das Gebiets Schema angepasst werden, in dem Sie ausgeführt werden. Diese Flexibilität ist wichtig, unabhängig davon, ob Sie Sie einer vorhandenen Anwendung hinzufügen oder Sie in eine neue Anwendung entwerfen.

Dieser Abschnitt unterstützt Sie beim Einstieg in die internationale Entwicklung. Es enthält Links zu Themen, in denen die Voraussetzungen für die Internationalisierung bereitgestellt werden. Es fasst die Technologien zusammen, die das SDK für die Unterstützung von weltweiten Kunden anbietet. Schließlich enthält dieser Abschnitt eine Beispielanwendung, die ein Problem löst, das beim Schreiben von globaler Software häufig auftritt.

## <a name="prerequisites"></a>Voraussetzungen

Sie sollten sich mit den Problemen vertraut machen, die bei der Entwicklung internationaler Software für Windows entstehen. Beginnen Sie mit diesen Übersichten.

-   Das [Verständnis der Internationalisierung](understanding-internationalization.md) erläutert die zusätzliche Schwierigkeit der Entwicklung weltweit einsatzbereiter Anwendungen und definiert wichtige Begriffe.
-   Das Thema " [Get World-Ready](https://msdn.microsoft.com/goglobal/bb895995.aspx) " führt Sie zu Richtlinien und bewährten Methoden, die Sie nach Bedarf durchlaufen oder nach Bedarf vertiefen können.
-   In der Prüfliste für die [Internationalisierung](internationalization-checklist.md) werden die Aktionen zusammengefasst, die Sie zum Erstellen einer weltweit einsetzbaren Anwendung
-   Sicherheit ist immer ein Problem bei der Softwareentwicklung. Sie müssen jedoch zusätzliche Probleme beim entwickeln internationaler Software in Erwägung gezogen. Sehen Sie sich die [Sicherheitsüberlegungen an: Internationale Features](security-considerations--international-features.md).

Beachten Sie auch die umfassenderen Artikel, die Sie im Abschnitt zum [globalen Entwickler Center von Go](https://msdn.microsoft.com/globalization/mt613165) in der [Globalisierung Schritt für Schritt](https://msdn.microsoft.com/globalization/mt642951) finden. Wenn Sie internationale Software entwickeln, sollten Sie sich die zusätzlichen Übersichten und detaillierten Artikel ansehen, die dort zu finden sind.

## <a name="learning-paths"></a>Lernpfade

Der Pfad, den Sie als nächstes lernen, um internationale Software zu erstellen, hängt von den Szenarien ab, denen Sie begegnen. Die folgenden Szenarios basieren auf den im Hauptabschnitt [Internationalisierungs Informationen für Windows-Anwendungen](international-support.md)eingeführten.

-   **Erstellen Sie Anwendungen, die in mehreren Regionen in mehreren Sprachen bereitgestellt werden können.**

    Die Herausforderung besteht darin, eine Anwendung zu entwickeln, die nicht für jede Sprache oder Kultur umgeschrieben werden muss.

    -   Lesen Sie den Artikel Grundlegendes zur [mehrsprachigen Benutzeroberfläche (MUI)](./about-multilingual-user-interface.md).
    -   Erkunden Sie die Dokumentation für die [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md).
    -   Beginnen Sie mit der [Hello MUI](#the-hello-mui-application) -Anwendung.

-   **Unterstützung der Eingabe und Anzeige von unterschiedlichen Sprachen, Zeichensätzen und Schriftarten.**

    Die Anwendung muss möglicherweise mehrere Zeichensätze unterstützen, komplexe Skripts unterstützen (z. b. solche, die zur Darstellung von Hebräisch, Arabisch, Thailändisch und indic verwendet werden), dem Benutzer die Auswahl aus internationalen Schriftarten erlauben oder dem Benutzer die Eingabe von Zeichen und Symbolen (z. b. japanischer Kanji) für andere Sprachen mithilfe einer Standardtastatur erlauben.

    -   Lesen Sie die folgenden Artikel:

        -   [Skript-und Schriftart Unterstützung in Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Eingabe Sprache: Tastaturen und IMEs](https://msdn.microsoft.com/globalization/mt662332)

    -   Erkunden Sie die Dokumentation zu:

        -   [Unicode und Zeichensätze](unicode-and-character-sets.md)
        -   [Internationale Schriftarten und Text Anzeige](international-fonts-and-text-display.md)
        -   [Eingabemethoden-Manager](input-method-manager.md)

-   **Anzeigen Kultur abhängiger Objekte in den entsprechenden Formaten.**

    Internationale Anwendungen sollten Gebiets Schema Einstellungen verwenden, um Zeichen folgen ordnungsgemäß zu sortieren und Kultur abhängige Informationen wie z. b. Zeit, Datumsangaben und Währungen anzuzeigen.

    -   Erkunden Sie das [Knowledge Center zur Unterstützung der Landessprache](./national-language-support-reference.md).
    -   Weitere Informationen finden Sie in der Dokumentation zur [Unterstützung der Landessprache (NLS)](national-language-support.md).

-   **Ermitteln Sie die vom Benutzer verwendete Sprache oder das Skript, und wenden Sie Sie auf die anderen Dienste der Anwendung an.**

    Wenn die Anwendung die Sprache ermitteln kann, in der Text-und Benutzereingaben geschrieben werden, können Inhalte wie Eingabe Aufforderungen oder Hilfe in einer verständlichen Sprache angezeigt werden.

    -   Lesen Sie den Artikel [Schreiben von weltweit einsatzfähigen Anwendungen in Windows: Erweiterte linguistische Dienste in Windows](./using-extended-linguistic-services.md).
    -   Erkunden Sie die Dokumentation für die [erweiterten linguistischen Dienste](extended-linguistic-services.md).

## <a name="internationalization-technologies-in-the-sdk"></a>Internationalisierungs Technologien im SDK

Der Abschnitt internationale Entwicklungsunterstützung des SDK stellt Technologien bereit, die es der Anwendung ermöglichen, Sprachen, Gebiets Schemas und Gebiets Schema spezifische Formate aufzuzählen. Sie können Sie in Microsoft Win32-Anwendungen verwenden, die Sie in C oder C++ schreiben.

Die [erweiterten linguistischen Dienste](extended-linguistic-services.md) bieten von Microsoft patentierte Technologien für die Identifizierung von Sprachen und Skripts in Text. Die Anwendung kann die verfügbaren Dienste basierend auf der Kategorie sowie auf Eingabe-und Ausgabesprache, Skript und Inhaltstyp bestimmen.

Die [Internationale Schriftarten und die Text Darstellung enthalten](international-fonts-and-text-display.md) Informationen über internationale Schriftarten, komplexe Skripts und Glyphen sowie die feine Darstellung von Typografiefunktionen auf der Windows-Plattform.

Der [Eingabemethoden-Manager (Character Method Manager, imm)](input-method-manager.md) ist eine Technologie, mit der die Anwendung Eingaben von der Eingabemethoden-Editor-Software (Input Method Editor, IME) empfängt, die wiederum den Eintrag von Zeichen und Symbolen (z. b. japanischer Kanji) für andere Sprachen mithilfe einer Standardtastatur zulässt.

## <a name="the-hello-mui-application"></a>Die Hello MUI-Anwendung

Eine gängige Aufgabe bei der internationalen Entwicklung beginnt mit einer monolingualen Anwendung, die Sie als weltweit bereitstellen müssen. Sie müssen Unterstützung für zusätzliche Sprachen hinzufügen, aber auf eine Weise, die nicht erfordert, dass Sie den Code für jede neue Sprache oder Kultur neu schreiben.

Diese Aufgabe bietet die Möglichkeit, ein Tutorial zu präsentieren, das Sie Schritt für Schritt durch die Erstellung einer Hello MUI-Anwendung führt und die Verwendung des MUI-Ressourcen Modells [(mehrsprachige Benutzeroberfläche)](multilingual-user-interface.md) und der zugehörigen Unterstützung in Windows ermöglicht.

Das Tutorial übernimmt das Konzept der vertrauten Hallo Welt Anwendung und demonstriert die Verwendung von MUI, um eine einfache mehrsprachige Anwendung zu erstellen.

Sie können das Hello MUI-Tutorial unter [Hinzufügen von Unterstützung für mehrsprachige Benutzeroberflächen zu einer Anwendung](creating-a-multilingual-user-interface-application.md)starten.

 

 
