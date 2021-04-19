---
title: CMM-Transformationserstellungsflags
description: CMMS verwenden Transformations Erstellungs Flags als Hinweise zum Erstellen einer Farb Transformation. Der CMM kann feststellen, wie diese Flags am besten verwendet werden.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106349750"
---
# <a name="cmm-transform-creation-flags"></a>CMM-Transformationserstellungsflags

CMMS verwenden Transformations Erstellungs Flags als Hinweise zum Erstellen einer Farb Transformation. Der CMM kann feststellen, wie diese Flags am besten verwendet werden.

Alle Funktionen, die diese Flags verwenden, übergeben oder empfangen Flagwerte über einen Parameter namens *dwFlags*. Das höchst wertige **Wort** von *dwFlags* sollte auf einen Wert aus der folgenden Tabelle festgelegt werden.



| Konstante                    | BESCHREIBUNG                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Aktivieren der über \_ Prüfung von Gamut \_     | Verwenden Sie diese Transformation für die Überprüfung der Überprüfung.                                                                                                       |
| \_relative \_ farbige Metrik verwenden | Behalten Sie den weißen Punkt nicht bei. Wenn der Ausgabe Farbskala eine angegebene Farbe nicht unterstützt, verwenden Sie die nächste unterstützte Farbe. Siehe Rendering Intents. |
| schnelles \_ übersetzen             | Nur Farbe suchen. Die Farbe kann nicht interpolieren werden.                                                                                            |
| Preserveblack               | Fügt die entsprechende "Black Generation GMMP" als letztes GMMP in der Transformations Sequenz ein.                                                     |
| immer WCS \_                 | Verwenden Sie den WCS-Codepfad auch für ICC-Transformationen.                                                                                               |
| sequenzielle \_ Transformation       | Transformations Erstellungs Flag zum Erstellen einer sequenziellen (nicht optimierten) Farb Transformation.                                                           |



 

Das nieder wertige **Wort** kann einen der folgenden Konstanten Werte aufweisen.



| Konstante     | BESCHREIBUNG                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| Nachweis \_ Modus  | Die Transformation wird verwendet, um eine Vorschau des Bilds anzuzeigen. Niedrige Bildqualität.                                    |
| normaler \_ Modus | Die Transformation wird für die normale Bild Anzeige verwendet. Durchschnittliche Bildqualität.                            |
| Bester \_ Modus   | Die Transformation wird für die Anzeige des qualitativ hochwertigen Bilds verwendet, das auf dem Zielgerät möglich ist. |



 

Wenn Sie vom Nachweis \_ Modus zum besten \_ Modus wechseln, wird die Ausgabequalität in der Regel verbessert, und die Transformations Geschwindigkeit wird

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[ICM-Konstanten](wcs-constants.md)
</dt> </dl>

 

 




