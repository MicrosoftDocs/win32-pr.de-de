---
description: Im folgenden Thema wird beschrieben, wie Sie eine einfache Wiedergabe ausführen.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Einfache Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351569"
---
# <a name="simple-playback"></a>Einfache Wiedergabe

Im folgenden Thema wird beschrieben, wie Sie eine einfache Wiedergabe ausführen.

**So führen Sie einfache Wiedergabe aus**

1.  Wählen Sie das Terminal Dateiwiedergabe auf der Ebene des Aufrufes aus.
2.  Erstellen Sie das Wiedergabe Terminal für den TAPI-Befehl.
3.  Legen Sie die Eigenschaften – Dateiname und Typ des Speichers fest.
4.  Öffnen Sie die [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) -Methode im Terminal der Dateiwiedergabe, um die Wiedergabe von Streams zu starten.

Der folgende Beispielcode veranschaulicht die einfache Wiedergabe.

Erstellen Sie zunächst das Terminal für die Aufzeichnung mithilfe der [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) -Schnittstelle. Dies weist den TSP/MSP an, die Dateiwiedergabe bei diesem-Befehl auszuführen. TSP/MSP erstellt ein Terminal, das von der Anwendung verwendet werden soll, und gibt es bei Erfolg zurück.


```C++

```



Holen Sie sich den [**itmediaplayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) -Schnittstellen Zeiger von der Terminal Schnittstelle, und verwenden Sie ihn, um den Dateinamen für die Wiedergabe festzulegen.


```C++
pMediaPlayback->Release();
```



Wenn die Datei einen Audiostream enthält und der-Befehl einen Audiodatenstrom aufzeichnen hat, wird der Audioinhalt in der Datei in diesem Stream wiedergegeben.

 

 



