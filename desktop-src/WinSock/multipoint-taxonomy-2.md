---
description: Die in diesem Abschnitt beschriebene Taxonomie unterscheidet zunächst die Steuerungsebene, die sich mit der Art und Weise befasst, wie eine Multipointsitzung eingerichtet wird, von der Datenebene, die sich mit der Übertragung von Daten zwischen Sitzungsteilnehmern befasst.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Multipoint-Taxonomie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1928dde2935ab803d95d73db225f7b3be0bc051a082d3bdae937e9b8e7da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097720"
---
# <a name="multipoint-taxonomy"></a>Multipoint-Taxonomie

Die in diesem Abschnitt beschriebene Taxonomie unterscheidet zunächst die Steuerungsebene, die sich mit der Art und Weise befasst, wie eine Multipointsitzung eingerichtet wird, von der Datenebene, die sich mit der Übertragung von Daten zwischen Sitzungsteilnehmern befasst.

## <a name="session-establishment-in-the-control-plane"></a>Sitzungseinrichtung in der Steuerungsebene

Auf der Steuerungsebene gibt es zwei unterschiedliche Arten der Sitzungseinrichtung:

-   Verwurzelt
-   nichtrooted

Im Fall der Root-Steuerung gibt es einen speziellen Teilnehmer, c root, der sich von den restlichen Mitgliedern dieser Multipointsitzung abschneidet, von denen jeder als \_ C-Blatt \_ bezeichnet wird. Der c-Stamm muss für die gesamte Dauer der Multipointsitzung vorhanden bleiben, da die Sitzung ohne den \_ c-Stamm zerbrochen \_ wird. Der c-Stamm initiiert in der Regel die Multipointsitzung, indem die Verbindung mit einem Blatt c oder einer Anzahl von \_ \_ \_ C-Blattknoten eingerichtet wird. Der c-Stamm kann weitere c-Blätter hinzufügen, oder (in einigen Fällen) kann ein c-Blatt zu einem späteren Zeitpunkt mit dem \_ \_ \_ \_ c-Stamm beitreten. Beispiele für die Steuerungsebene mit Stamm sind in ATM und ST-II zu finden.

Bei einer steuerungsebene ohne Stamm sind alle Mitglieder, die zu einer Multipointsitzung gehören, Blättern, d. B. es gibt keinen speziellen Teilnehmer, der als \_ c-Stamm agiert. Jedes c-Blatt muss sich selbst zu einer bereits vorhandene Multipointsitzung hinzufügen, die immer verfügbar ist (wie bei einer IP-Multicastadresse) oder über einen Out-of-Band-Mechanismus (OOB) eingerichtet wurde, der außerhalb des Bereichs der \_ Windows Sockets-Spezifikation liegt.

Eine weitere Möglichkeit, dies zu betrachten, ist, dass ein c-Stamm immer noch vorhanden ist, aber als in der Netzwerk-Cloud im Gegensatz zu einem \_ der Teilnehmer betrachtet werden kann. Da immer noch ein Steuerelementstamm vorhanden ist, kann auch eine Nichtstammsteuerungsebene als implizite Stammebene betrachtet werden. Beispiele für diese Art von impliziten Multipointschemas sind:

-   Eine Teleferencing-Brücke.
-   Das IP-Multicastsystem.
-   Eine Multipoint Control Unit (MCU) in einer H.320-Videokonferenz.

## <a name="data-transfer-in-the-data-plane"></a>Datenübertragung auf der Datenebene

Auf der Datenebene gibt es zwei Arten von Datenübertragungsstilen:

-   Verwurzelt
-   nichtrooted

Auf einer Datenebene mit Rooting ist ein spezieller Teilnehmer namens d \_ root vorhanden. Die Datenübertragung erfolgt nur zwischen dem Stamm d und den restlichen Mitgliedern dieser Multipointsitzung, die jeweils als \_ Blatt d bezeichnet \_ werden. Der Datenverkehr kann unidirektional oder bidirektional sein. Die vom d-Stamm gesendeten Daten werden dupliziert (falls erforderlich) und an jedes Blatt d übermittelt, während die Daten von d Leafs nur an den \_ \_ \_ d-Stamm \_ gesendet werden. Im Fall einer Datenebene mit Stamm ist kein Datenverkehr zwischen \_ D-Blatt zugelassen. Ein Beispiel für ein Protokoll, das auf der Datenebene basiert, ist ST-II.

Auf einer Nicht-Rooted-Datenebene sind alle Teilnehmer gleich, d.&a; alle daten, die sie senden, werden an alle anderen Teilnehmer derselben Multipointsitzung übermittelt. Ebenso kann jeder Blattknoten Daten von allen anderen Blattknoten und in einigen Fällen von anderen Knoten empfangen, die nicht an der \_ \_ Multipointsitzung teilnehmen. Es ist kein spezieller \_ d-Stammknoten vorhanden. IP-Multicast ist in der Datenebene nichtrooted.

Beachten Sie, dass die Frage, wo dateneinheitsdupliziert wird oder ob eine freigegebene einzelne Struktur oder mehrere Strukturen mit dem kürzesten Pfad für die Multipointverteilung verwendet werden, Protokollprobleme sind und für die Schnittstelle, die die Anwendung für die Multipointkommunikation verwenden würde, irrelevant ist. Daher werden diese Probleme in diesem Anhang oder in der Windows Sockets-Schnittstelle nicht behandelt.

Die folgende Tabelle zeigt die oben beschriebene Taxonomie und gibt an, wie vorhandene Schemas in die einzelnen Kategorien passen. Beachten Sie, dass es keine vorhandenen Schemas zu geben scheint, die eine nichtrooted-Steuerungsebene zusammen mit einer Stammdatenebene verwenden.

|                      | Steuerungsebene mit Stamm | Steuerungsebene ohne Stamm (implizite Stammsteuerung) |
|----------------------|----------------------|-------------------------------------------|
| Datenebene mit Stamm    | ATM, ST-II           | Keine bekannten Beispiele.                        |
| Nicht rootierte Datenebene | T.120                | IP-Multicast, H.320 (MCU)                 |



 

 

 



