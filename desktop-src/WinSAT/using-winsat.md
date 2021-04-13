---
title: Verwenden von WinSAT
description: Mithilfe der Windows-System Bewertungs Tool-API (WinSAT) können Sie formale und Ad-hoc-Bewertungen der Hardwarekonfiguration des Computers initiieren, das Basisergebnis für den Computer und die Ergebnisse für jede Unterkomponente der Bewertung abrufen und die Details der Bewertung abrufen, z. b. die Details des bewerteten Prozessors.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a23ab35d989a736fa61833e678c0a4c79954e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388211"
---
# <a name="using-winsat"></a>Verwenden von WinSAT

\[WinSAT kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.\]

Mithilfe der Windows-System Bewertungs Tool-API (WinSAT) können Sie [formale und Ad-hoc-Bewertungen](#initiating-an-assessment) der Hardwarekonfiguration des Computers initiieren, [das Basisergebnis für den Computer](#retrieving-the-scores-of-the-assessment) und die Ergebnisse für jede Unterkomponente der Bewertung abrufen und die [Details der Bewertung abrufen](#retrieving-details-of-the-assessment), z. b. die Details des bewerteten Prozessors.

## <a name="initiating-an-assessment"></a>Initiieren einer Bewertung

Nachdem Windows 8.1 können Sie formale und Ad-hoc-Bewertungen des Computers initiieren. Bei einer formalen Bewertung werden die folgenden unter Komponenten des Computers bewertet:

-   CPU
-   Arbeitsspeicher
-   Primary disk
-   Grafikkarte

Zum Initiieren einer formalen Bewertung müssen Sie die [**iinitiatewinsatassessment:: initiateformalassessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) -Methode aufrufen. Die Ergebnisse formaler Bewertungen werden im Bewertungs Speicher gespeichert und können zu einem späteren Zeitpunkt abgerufen werden.

In der Regel werden Ad-hoc-Bewertungen verwendet, um nur eine Unterkomponente des Computers zu bewerten, z. b. die CPU oder den Arbeitsspeicher. Sie können jedoch den **formalen** Switch verwenden, um alle unter Komponenten zu bewerten. Um eine Ad-hoc-Bewertung zu initiieren, müssen Sie die [**iinitiatewinsatassessment:: initiateassessment**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) -Methode aufrufen. Beachten Sie, dass die Ergebnisse von Ad-hoc-Bewertungen nicht im Bewertungs Speicher gespeichert werden.

Um die Benachrichtigung abzurufen, wenn der Fortschritt erfolgt oder die Bewertung abgeschlossen ist, implementieren Sie die [**iwinsatinitiateevents**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) -Schnittstelle.

Sie können keine formalen Bewertungen Remote oder auf einem Computer ausführen, auf dem unter Batterien ausgeführt wird. Sie können auch keine Ad-hoc-Bewertung für die Grafik Unterkomponente ausführen.

## <a name="retrieving-the-scores-of-the-assessment"></a>Abrufen der Bewertungen der Bewertung

Sie können das Basisergebnis des Computers und das Ergebnis für jede Unterkomponente der Bewertung abrufen. Sie können die-API verwenden, um die Ergebnisse nur für formale Bewertungen abzurufen. Zum Abrufen der Ergebnisse für Ad-hoc-Bewertungen müssen Sie das **-XML-** Argument in der Befehlszeile einschließen, um die Bewertungsergebnisse in einer XML-Datei zu speichern und dann die Datei für das Ergebnis der Unterkomponente zu analysieren.

Die Basisbewertung ist eine allgemeine Messung der Hardwarekonfiguration des Computers. Eine höhere Basisbewertung bedeutet im Allgemeinen, dass der Computer besser und schneller als ein Computer mit einer niedrigeren Basisbewertung ausgeführt werden kann, insbesondere wenn erweiterte und ressourcenintensive Aufgaben ausgeführt werden.

Jede Hardwarekomponente erhält eine einzelne Teilbewertung. Die Basisbewertung des Computers wird durch das niedrigste Teilergebnis bestimmt. Wenn z. b. das niedrigste Teilergebnis einer einzelnen Hardwarekomponente 2,6 ist, ist die Basisbewertung 2,6. Das Basisergebnis ist kein Mittelwert der kombinierten Teilergebnisse.

Ein Benutzer kann mit dem Basisergebnis zuverlässig Programme und andere Software kaufen, die mit der Basisbewertung des Computers übereinstimmen. Wenn der Computer z. b. eine Basisbewertung von 3,3 hat, kann der Benutzer zuverlässig jede Software erwerben, die für diese Version von Windows entwickelt wurde und einen Computer mit einer Basisbewertung von 3 oder niedriger erfordert.

Um das Basisergebnis abzurufen, rufen Sie zuerst die [**iqueryrecentwinsatassessment:: get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) -Methode auf, um die [**iprovidewinsatresultsinfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) -Schnittstelle abzurufen. Anschließend können Sie die [**iprovidewinsatresultsinfo:: get \_ systemrating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) -Methode aufrufen, um das Basisergebnis zu erhalten.

Ein Benutzer kann anhand der unter Komponenten Bewertungen ermitteln, ob eine Unterkomponente des Computers einen bestimmten Anwendungstyp unterstützen kann. Beispielsweise kann ein Benutzer, der mehr Zeit für das Lesen oder Schreiben von Dokumenten verbringt, eine höhere Bewertung für den Datenträger als ein Benutzer, der wissenschaftliche Anwendungen ausführt, und ein Benutzer, der wissenschaftliche Anwendungen ausführt, eine höhere CPU-unter Komponenten Bewertung benötigen und sich möglicherweise nicht mit einer geringeren Datenträger Bewertung befassen.

Um das Ergebnis für jede Unterkomponente abzurufen, rufen Sie zuerst die [**iqueryrecentwinsatassessment:: get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) -Methode auf, um die [**iprovidewinsatresultsinfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) -Schnittstelle abzurufen. Anschließend können Sie die [**iprovidewinsatresultsinfo:: getgutamentinfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) -Methode aufrufen, um die [**iprovidewinsatbewermentinfo**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) -Schnittstelle abzurufen. Rufen Sie für jede Unterkomponente, deren Ergebnis Sie abrufen möchten, die [**iprovidewinsatbewermentinfo:: get \_ Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) -Methode auf.

## <a name="retrieving-details-of-the-assessment"></a>Abrufen der Details der Bewertung

Die WinSAT-API stellt die Gesamtbewertung und die Gesamtergebnisse für jede Unterkomponente bereit. Zum Abrufen der Details der Bewertung (z. b. der Metriken, die zum Berechnen des Ergebnisses und der Details des bewerteten Prozessors verwendet werden), müssen Sie die Daten aus dem XML-Bewertungsdokument abrufen. Rufen Sie zum Abrufen der Details der letzten formalen Bewertung die [**iqueryrecentwinsatassessment:: get \_ XML**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) -Methode auf. Um die Details aus jeder Bewertung im WinSAT-Datenspeicher abzurufen, rufen Sie die [**iqueryallwinsatassessments:: get \_ allxml**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) -Methode auf.

Weitere Informationen zum XML-Schema und den Details, die Sie abrufen können, finden Sie unter [WinSAT-Schema](winsat-schema.md).

 

 




