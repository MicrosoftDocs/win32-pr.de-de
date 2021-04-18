---
description: Tablet PC umfasst Technologie zum Erkennen von frei Hand Eingaben, die in der Regel in Form von Handschrift vorliegt.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informationen zur Handschrifterkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352798"
---
# <a name="about-handwriting-recognition"></a>Informationen zur Handschrifterkennung

Tablet PC umfasst Technologie zum Erkennen von frei Hand Eingaben, die in der Regel in Form von Handschrift vorliegt. Das Softwaremodul, das die Erkennung bereitstellt, wird als Erkennungs Modul bezeichnet. Eine Erkennung erkennt eine Sprache, eine Gruppe verwandter Sprachen oder eine Klasse verwandter Objekte wie z. b. Musik Notizen, System Gesten oder geometrische Formen. Sie können erkenungen dynamisch dem Ink Services-System hinzufügen.

## <a name="recognition-steps"></a>Erkennungs Schritte

Die Erkennung wird durch die Verwendung eines Erkennungs Kontexts behandelt. Die Erkennung besteht aus vier grundlegenden Schritten:

1.  Einrichten der Erkennungs Einschränkungen durch:
    -   Auswählen der Erkennungs-und Eingabemodus (geometrische Einschränkungen).
    -   Festlegen der Spracheinschränkungen. Beispielsweise können Sie die Eingabe auf alphanumerische Zeichen einschränken oder Schemas übergeben, um die Erkennung zu unterstützen.
2.  Senden von frei Hand Eingaben an die Erkennung.
3.  Verarbeiten der Eingabe (erkennen).
4.  Zurückgeben der Ergebnisse der Erkennung.

Die Schritte 2 und 3 werden möglicherweise in einer Schleife wiederholt, oder alle frei Hand Eingaben werden möglicherweise dem frei Hand Eingaben hinzugefügt, bevor ein Erkennungs Versuch erfolgt.

## <a name="samples-and-related-topics"></a>Beispiele und Verwandte Themen

Das [Beispiel "Advanced Recognition](advanced-recognition-sample.md) " veranschaulicht, wie Erkennungs [**Tools mit frei**](inkdisp-class.md) Hand Objekten verwendet werden, um eine frei Handerkennung auszuführen

Die [Beispiel Vorlage der Erkennungs](recognizer-dll-sample-template.md) Modul-dll enthält eine Vorlage zum Erstellen einer Erkennungs-DLL. Die Vorlage enthält Funktionen zum Registrieren und Aufheben der Registrierung des Servers sowie zu den Skeletten für primäre Erkennungsfunktionen.

In den folgenden Abschnitten werden die grundlegenden Konzepte hinter der Tablet PC-Erkennungstechnologie beschrieben. Ausführliche Informationen zum Erstellen von benutzerdefinierten erkenzern finden Sie unter [Erstellen einer Erkennung](creating-a-recognizer.md).

-   [Text erkenzer](text-recognizers.md)
-   [Objekterkenzer](object-recognizers.md)
-   [Verwenden der Erkennungs Sammlung](using-the-recognizers-collection.md)
-   [Erkennungs Kontext](recognizer-context.md)
-   [Erkennungs Segmente](recognition-segments.md)
-   [Erkennung von Abgewinkelter Text](recognition-of-angled-text.md)
-   [Unterstützung für das Unterzeichnen von Stroke-Befehlen](recognizer-stroke-reordering-support.md)
-   [Wörterbücher und Faktoide](dictionaries-and-factoids.md)
-   [Vertrauens Eigenschaft \[ für die Erkennung\]](confidence-property--about-recognition.md)
-   [Alternative Stile](alternates.md)
-   [Frei Hand Segmente und-Alternativen](ink-segments-and-alternates.md)

 

 



