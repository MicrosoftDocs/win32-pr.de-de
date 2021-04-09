---
description: Dieses Thema enthält eine Prozedur zum Durchführen einer Nachverfolgung gesteuerten Aufzeichnung von Audiodatenströmen.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled Datensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865688"
---
# <a name="track-controlled-record"></a>Track-Controlled Datensatz

Dieses Thema enthält eine Prozedur zum Durchführen einer Nachverfolgung gesteuerten Aufzeichnung von Audiodatenströmen.

**So führen Sie eine Nachverfolgung gesteuerte Aufzeichnung von Audiostreams durch**

1.  Wählen Sie Datei nachverfolgen Terminals in Streams aus.
2.  Erstellen Sie das Terminal für den Datei Daten Satz.
3.  Legen Sie den Dateinamen fest.
4.  Enumerieren von Streams für den TAPI-Befehl. Informationen zu diesen Schritten finden Sie im folgenden Verfahren.
5.  Ruft die [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) -Methode für das Terminal Datei Daten Satz ab, um die Datenstrom Aufzeichnung zu starten

**So zählen Sie Streams für den TAPI-Befehl auf**

1.  Erstellen Sie eine Spur desselben audiotyps und derselben Richtung wie der Stream.
2.  Legen Sie die Track-Eigenschaften für das Audioformat fest. Wenn nicht festgelegt, ist das Format mit dem Stream-Format identisch.
3.  Wählen Sie den Track im Stream aus.

Wenn eine Spur in mehreren Streams ausgewählt ist, bedeutet dies, dass Datenströme gemischt werden.

 

 



