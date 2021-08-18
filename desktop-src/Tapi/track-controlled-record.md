---
description: Dieses Thema enthält ein Verfahren zum Ausführen einer trackgesteuerten Aufzeichnung von Audiostreams.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled Datensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499c4cb79015effa80add4fc5369ec53f134e83f3f1b7e4cda06b09869c01386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872670"
---
# <a name="track-controlled-record"></a>Track-Controlled Datensatz

Dieses Thema enthält ein Verfahren zum Ausführen einer trackgesteuerten Aufzeichnung von Audiostreams.

**So führen Sie die trackgesteuerte Aufzeichnung von Audiostreams aus**

1.  Wählen Sie Terminale in Streams nachverfolgen aus.
2.  Erstellen Sie das Dateidatensatz-Terminal.
3.  Legen Sie den Dateinamen fest.
4.  Aufzählen von Streams beim TAPI-Aufruf. Diese Schritte finden Sie im folgenden Verfahren.
5.  Rufen Sie die [**Start-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) im Dateidatensatzterminal auf, um die Streamaufzeichnung zu starten.

**So aufzählen Sie Datenströme für den TAPI-Aufruf**

1.  Erstellen Sie eine Spur desselben Audiotyps und derselben Richtung wie der Stream.
2.  Legen Sie die Trackeigenschaften für das Audioformat fest. Wenn diese Einstellung nicht festgelegt ist, ist das Format mit dem Streamformat identisch.
3.  Wählen Sie die Spur im Stream aus.

Wenn eine Spur in mehreren Streams ausgewählt ist, impliziert dies das Mischen von Streams.

 

 



