---
title: Dokument als Momentaufnahme von Eigenschaften
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393882"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Printfunktionalitäten-Dokument als Momentaufnahme von Eigenschaften

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das Gerät, das von PrintProperties beschrieben wird, verfügt möglicherweise über Eigenschaften, die vom Zustand oder der Konfiguration des Geräts abhängig sind. Obwohl printfunktionen den vollständigen Konfigurationsbereich eines Geräts darstellt, erzeugt der Printworks-Anbieter eine Konfigurations abhängige Instanz der Print-Funktionen, die als printfunktionalitäten-Dokument bezeichnet werden. Dieses Konfigurations abhängige Printworks-Dokument vermeidet, das printfunktionalitäten-Schema durch die Komplexität der Darstellung mehr wertiger Daten zu belasten. Noch wichtiger ist, dass es für alle Eigenschaften-und ScoredProperty-Instanzen in einem printfunktionalitäten-Dokument einwertig sein muss, um einen Consumer des Printworks-Dokuments von der Aufgabe zu entlasten, den entsprechenden Wert aus einer mehrwertigen Datendarstellung zu extrahieren. Anders ausgedrückt: jede Eigenschaft und eine ScoredProperty-Instanz in einem Printworks-Dokument müssen einen Fixed-Wert aufweisen, der relativ zur Eingabe Konfiguration ist. Jedes Dokument von printfunktionen kann als eine Momentaufnahme der Eigenschaften des Geräts betrachtet werden, wenn sich das Gerät in einem bestimmten Zustand befindet. Folglich muss die zu verwendende Konfiguration bereitgestellt werden, bevor ein printfunktionalitäten-Dokument erstellt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



