---
title: Verwenden von WinSAT
description: Sie können die Windows System Assessment Tool (WinSAT)-API verwenden, um formale und Ad-hoc-Bewertungen der Hardwarekonfiguration des Computers zu initiieren, die Basisbewertung für den Computer und die Bewertungen für die einzelnen Unterkomponenten der Bewertung abzurufen und Details der Bewertung abzurufen, z. B. die Details des bewerteten Prozessors.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23cf26d31ccbd3eb6e51fb1717c055fb6538c57612d374b0a3b7a2a5b2382681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733780"
---
# <a name="using-winsat"></a>Verwenden von WinSAT

\[WinSAT kann nach der Veröffentlichung geändert oder nicht mehr Windows 8.1.\]

Sie können die Windows System Assessment Tool (WinSAT)-API verwenden, um [formale](#initiating-an-assessment) und Ad-hoc-Bewertungen der Hardwarekonfiguration des Computers zu [initiieren,](#retrieving-the-scores-of-the-assessment) die Basisbewertung für den Computer und die Bewertungen für die einzelnen Unterkomponenten der Bewertung abzurufen und Details zur Bewertung [abzurufen,](#retrieving-details-of-the-assessment)z. B. die Details des bewerteten Prozessors.

## <a name="initiating-an-assessment"></a>Initiieren einer Bewertung

Nach Windows 8.1 können Sie formale und Ad-hoc-Bewertungen des Computers initiieren. Eine formale Bewertung bewertet die folgenden Unterkomponenten des Computers:

-   CPU
-   Arbeitsspeicher
-   Primary disk
-   Grafikkarte

Um eine formale Bewertung zu initiieren, rufen Sie die [**IInitiateWinSATAssessment::InitiateFormalAssessment-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) auf. Die Ergebnisse formaler Bewertungen werden im Bewertungsspeicher gespeichert und können zu einem späteren Zeitpunkt abgerufen werden.

In der Regel verwenden Sie Ad-hoc-Bewertungen, um nur eine Unterkomponenten des Computers zu bewerten, z. B. die CPU oder den Arbeitsspeicher. Sie können jedoch den formalen **Schalter verwenden,** um alle Unterkomponenten zu bewerten. Um eine Ad-hoc-Bewertung zu initiieren, rufen Sie die [**IInitiateWinSATAssessment::InitiateAssessment-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) auf. Beachten Sie, dass die Ergebnisse von Ad-hoc-Bewertungen nicht im Bewertungsspeicher gespeichert werden.

Implementieren Sie die [**IWinSATInitiateEvents-Schnittstelle,**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents) um eine Benachrichtigung abzurufen, wenn der Fortschritt erfolgt oder die Bewertung abgeschlossen ist.

Sie können keine formalen Bewertungen remote oder auf einem Computer ausführen, der auf Akkus ausgeführt wird. Sie können auch keine Ad-hoc-Bewertung für die Grafikunterkomponenten remote ausführen.

## <a name="retrieving-the-scores-of-the-assessment"></a>Abrufen der Bewertungen der Bewertung

Sie können die Basisbewertung des Computers und die Bewertung für jede Unterkomponenten der Bewertung abrufen. Sie können die API verwenden, um die Bewertungen nur für formale Bewertungen abzurufen. Um die Bewertungen für Ad-hoc-Bewertungen abzurufen, müssen Sie das **Argument -xml** in die Befehlszeile einfassen, um die Bewertungsergebnisse in einer XML-Datei zu speichern und dann die Datei auf die Bewertung der Unterkomponenten zu analysieren.

Die Basispunktzahl ist eine allgemeine Messung der Hardwarekonfiguration des Computers. Eine höhere Basispunktzahl bedeutet in der Regel, dass der Computer eine bessere und schnellere Leistung erzielt als ein Computer mit einer niedrigeren Basispunktzahl, insbesondere bei erweiterten und ressourcenintensiveren Aufgaben.

Jede Hardwarekomponente erhält einen einzelnen Subscore. Die Basispunktzahl Ihres Computers wird durch den niedrigsten Subscore bestimmt. Wenn der niedrigste Subscore einer einzelnen Hardwarekomponente beispielsweise 2,6 ist, beträgt die Basispunktzahl 2,6. Die Basispunktzahl ist kein Durchschnitt der kombinierten Untergeordneten Kerne.

Ein Benutzer kann die Basispunktzahl verwenden, um sicher Programme und andere Software zu kaufen, die mit der Basispunktzahl ihres Computers übereinstimmen. Wenn der Computer z. B. über eine Basisnote von 3,3 verfügt, kann der Benutzer jede Software, die für diese Version von Windows entwickelt wurde und einen Computer mit einer Basispunktzahl von 3 oder niedriger erfordert, sicher erwerben.

Rufen Sie zum Abrufen der Basisbewertung zunächst die [**IQueryRecentWinSATAssessment::get \_ Info-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) auf, um die [**IProvideWinSATResultsInfo-Schnittstelle**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) abzurufen. Rufen Sie dann die [**IProvideWinSATResultsInfo::get \_ SystemRating-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) auf, um die Basispunktzahl zu erhalten.

Ein Benutzer kann Unterkomponentenergebnisse verwenden, um zu bestimmen, ob eine Unterkomponenten des Computers einen bestimmten Anwendungstyp unterstützen kann. Beispielsweise kann ein Benutzer, der mehr Zeit mit dem Lesen oder Schreiben von Dokumenten verbringt, eine höhere Bewertung für den Datenträger benötigen als ein Benutzer, der wissenschaftliche Anwendungen ausgeführt, und ein Benutzer, der wissenschaftliche Anwendungen ausgeführt, würde wahrscheinlich eine höhere CPU-Unterkomponenten-Bewertung wünschen und sich möglicherweise nicht um eine niedrigere Datenträger-Bewertung sorgen.

Um die Bewertung für jede Unterkomponenten abzurufen, rufen Sie zunächst die [**IQueryRecentWinSATAssessment::get \_ Info-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) auf, um die [**IProvideWinSATResultsInfo-Schnittstelle abzurufen.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) Rufen Sie dann die [**IProvideWinSATResultsInfo::GetAssessmentInfo-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) auf, um die [**IProvideWinSATAssessmentInfo-Schnittstelle**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) zu erhalten. Rufen Sie für jede Unterkomponenten, deren Bewertung Sie abrufen möchten, die [**IProvideWinSATAssessmentInfo::get \_ Score-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) auf.

## <a name="retrieving-details-of-the-assessment"></a>Abrufen von Details der Bewertung

Die WinSAT-API stellt die Allgemeine Basisbewertung und die Bewertungen für jede Unterkomponenten bereit. Sie müssen die Daten aus dem XML-Bewertungsdokument abrufen, um Details zur Bewertung abzurufen (z. B. die Metriken, die zum Berechnen der Bewertung und der Details des bewerteten Prozessors verwendet werden). Um Details zur letzten formalen Bewertung abzurufen, rufen Sie die [**IQueryRecentWinSATAssessment::get \_ XML-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) auf. Um die Details aus jeder Bewertung im WinSAT-Datenspeicher abzurufen, rufen Sie die [**IQueryAllWinSATAssessments::get \_ AllXML-Methode**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml) auf.

Informationen zum XML-Schema und den Details, die Sie abrufen können, finden Sie unter [WinSAT-Schema](winsat-schema.md).

 

 




