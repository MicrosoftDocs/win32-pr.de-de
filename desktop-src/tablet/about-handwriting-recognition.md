---
description: Tablet PC enthält Technologie zum Erkennen von Ink-Eingaben, die am häufigsten in Form von Handschrift verwendet wird.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informationen zur Handschrifterkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4106d887eaa5bae2a162ab3c08a42c0d3b425b05a09b50bfcde626c05707f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884050"
---
# <a name="about-handwriting-recognition"></a>Informationen zur Handschrifterkennung

Tablet PC enthält Technologie zum Erkennen von Ink-Eingaben, die am häufigsten in Form von Handschrift verwendet wird. Das Softwaremodul, das die Erkennung bietet, wird als Erkennung bezeichnet. Eine Recognizer erkennt eine Sprache, eine Gruppe verwandter Sprachen oder eine Klasse verwandter Objekte, z. B. Musiknoten, Systemgesten oder geometrische Formen. Sie können dem Ink-Dienstsystem dynamisch Wiedererkenner hinzufügen.

## <a name="recognition-steps"></a>Erkennungsschritte

Die Erkennung wird durch die Verwendung eines Erkennungskontexts behandelt. Die Erkennung besteht aus vier grundlegenden Schritten:

1.  Einrichten der Erkennungseinschränkungen durch:
    -   Auswählen des Recognizer- und Eingabemodus (geometrische Einschränkungen).
    -   Festlegen der Spracheinschränkungen. Beispielsweise können Sie die Eingabe auf alphanumerische Zeichen beschränken oder Schemas übergeben, um die Suche zu unterstützen.
2.  Senden von Ink an die Recognizer-Datei.
3.  Verarbeiten der Eingabe (Erkennen).
4.  Zurückgeben der Ergebnisse der Erkennung.

Die Schritte 2 und 3 können in einer Schleife wiederholt werden, oder alle Ink-Striche können der Ink hinzugefügt werden, bevor versucht wird, die Erkennung zu versuchen.

## <a name="samples-and-related-topics"></a>Beispiele und verwandte Themen

[Das Erweiterte Erkennungsbeispiel](advanced-recognition-sample.md) veranschaulicht, wie Erkennungen mit [**Ink-Objekten verwendet**](inkdisp-class.md) werden, um die Ink-Erkennung durchzuführen.

[Die Beispielvorlage für die Recognizer-DLL](recognizer-dll-sample-template.md) enthält eine Vorlage zum Erstellen einer Recognizer-DLL. Die Vorlage enthält Funktionen zum Registrieren und Aufheben der Registrierung des Servers sowie Gerüste für primäre Recognizer-Funktionen.

In den folgenden Abschnitten werden die grundlegenden Konzepte der Tablet PC-Erkennungstechnologie beschrieben. Ausführliche Informationen zum Erstellen benutzerdefinierter Recognizer finden Sie unter [Creating a Recognizer](creating-a-recognizer.md).

-   [Text-Recognizers](text-recognizers.md)
-   [Objekt-Recognizers](object-recognizers.md)
-   [Verwenden der Recognizers-Auflistung](using-the-recognizers-collection.md)
-   [Kontext der Wiedererkennung](recognizer-context.md)
-   [Erkennungssegmente](recognition-segments.md)
-   [Erkennung von winkeliertem Text](recognition-of-angled-text.md)
-   [Unterstützung für die Neuanordnung von Strichen in der Wiedererkennung](recognizer-stroke-reordering-support.md)
-   [Wörterbücher und Factoide](dictionaries-and-factoids.md)
-   [Confidence-Eigenschaft \[ zur Erkennung\]](confidence-property--about-recognition.md)
-   [Alternative Stile](alternates.md)
-   [Ink Segments and Alternates](ink-segments-and-alternates.md)

 

 



