---
title: Abspielen von Dateien aus einer Netzwerkquelle
description: Abspielen von Dateien aus einer Netzwerkquelle
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows Media-Format-SDK, Lesen von ASF-Daten
- Windows Media-Format-SDK, Abspielen von Dateien aus Netzwerk Quellen
- Advanced Systems Format (ASF), Lesen von Daten
- ASF (Advanced Systems Format), Lesen von Daten
- Advanced Systems Format (ASF), Abspielen von Dateien aus Netzwerk Quellen
- ASF (Advanced Systems Format), Abspielen von Dateien aus Netzwerk Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1e4e41ddf94498ddeddf90e64439c1b11b7ba8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106341706"
---
# <a name="playing-files-from-a-network-source"></a>Abspielen von Dateien aus einer Netzwerkquelle

Das Lesen aus einem Netzwerk unterscheidet sich nicht grundlegend von dem Lesen einer lokalen Datei. Die Anwendung übergibt die URL an die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode des Reader-Objekts, und das Reader-Objekt verarbeitet die Details der Netzwerkprotokolle. Das Reader-Objekt verwendet die intelligente Puffer Verwaltung, um die optimale Wiedergabe zu ermöglichen. Wenn die Anwendung mehr Kontrolle über die Netzwerkeinstellungen des Reader-Objekts benötigt, sind diese über die [**iwmreadernetworkconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) -und [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) -Schnittstelle verfügbar.

Inhalte aus einer Netzwerkquelle fallen in eine der folgenden beiden Kategorien:

-   -. Die Daten werden direkt übermittelt, um auf dem lokalen Computer wiedergegeben zu werden. Server mit Windows Media Services können Streamingdaten bereitstellen. Wenn der MBR-Inhalt (Multiple Bitrate) gestreamt wird, kann der Client beim Fortschreiten des Streamings eine andere Bitrate vom Server anfordern.
-   Finden. Alle Daten werden so schnell wie möglich übertragen, sodass Sie als Datei auf dem lokalen Computer gespeichert werden können. Webserver stellen heruntergeladene Daten bereit. Nachdem der Download begonnen hat, erfolgt keine Kommunikation zwischen dem Client und dem Server.

Wenn das Reader-Objekt eine Datei von einem Webserver herunterlädt, wird ein Verfahren mit dem Namen progressives Streaming verwendet, mit dem ein Spieler mit dem Rendern des Inhalts beginnen kann, bevor der Download beendet ist. Die Daten werden gepuffert, um einen ununterbrochenen Datenfluss an den Player zu liefern. Informationen wie die Übertragungsrate und die Dauer des Inhalts werden verwendet, um zu bestimmen, wie lange die Daten gepuffert werden sollen, bevor Sie an den Player übergeben werden.

Um eine Datei oder einen Stream über ein Netzwerk zu öffnen, müssen Sie die **iwmreader:: Open** -Methode des Reader-Objekts mit der entsprechenden URL aufzurufen. **Open** ist ein asynchroner Rückruf, der sofort zurückgegeben wird. Wenn die Quelle zum Lesen bereit ist, sendet das Reader-Objekt eine per WMT \_ geöffnete Benachrichtigung an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode der Anwendung. An diesem Punkt kann die Anwendung den Reader durch Aufrufen von [**IWMReaderAdvanced2:: getplaymode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)für den Übermittlungs Modus Abfragen. Für den Netzwerk Inhalt gibt diese Methode entweder den Download Modus von WMT zurück, gibt den \_ \_ \_ heruntergeladenen Inhalt an, oder das Streaming im WMT- \_ Wiedergabe \_ Modus \_ , was den Streaming-Inhalt anzeigt.

Um mit dem Lesen der Datei oder des Streams zu beginnen, müssen Sie die [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) -Methode abrufen. Der Reader sendet eine \_ \_ Start Benachrichtigung für den WMT-Puffer, wenn er mit dem Puffern des Inhalts beginnt, und eine Benachrichtigung zum Beenden von WMT- \_ Pufferungen, wenn die \_ Pufferung beendet ist. Während der Reader den Inhalt puffert (also zwischen diesen beiden Benachrichtigungen), empfiehlt es sich, den Puffer Status für den Benutzer anzuzeigen. Die [**IWMReaderAdvanced2:: getbufferprogress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) -Methode gibt den Prozentsatz der gepufferten Daten und die geschätzte verbleibende Zeit zurück. Für den heruntergeladenen Inhalt können Sie auch [**IWMReaderAdvanced2:: getdownloadprogress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) aufrufen, um den Download Fortschritt zu erhalten. Aufrufen Sie diese Methoden wiederholt, um die Anzeige zu aktualisieren, bis die Pufferung abgeschlossen ist. Die Pufferung kann während der Wiedergabe aufgrund von Faktoren wie der Überlastung des Netzwerks wiederholt erfolgen. Wenn dies der Fall ist, empfängt die Anwendung eine andere Start Benachrichtigung für den WMT- \_ Puffer \_ .

Wenn das Reader-Objekt mit der Wiedergabe des Inhalts beginnt, sendet es eine WMT-Benachrichtigung, die \_ gestartet wurde. Da jedes Beispiel decodiert wird und für das Rendering verfügbar ist, übergibt der Reader es über die [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) Callback-Methode an die Anwendung. An diesem Punkt ist der Prozess der gleiche wie bei der lokalen Dateiwiedergabe. Wenn die Wiedergabe angehalten wird, sendet der Reader ein WMT- \_ Ende \_ der \_ Streaming-Benachrichtigung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




