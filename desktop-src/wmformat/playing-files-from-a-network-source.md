---
title: Wiederspielen von Dateien aus einer Netzwerkquelle
description: Wiederspielen von Dateien aus einer Netzwerkquelle
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows Medienformat-SDK, Lesen von ASF-Daten
- Windows Medienformat-SDK, Wiedergabe von Dateien aus Netzwerkquellen
- Advanced Systems Format (ASF), Lesen von Daten
- ASF (Advanced Systems Format), Lesen von Daten
- Advanced Systems Format (ASF), Wiedergabe von Dateien aus Netzwerkquellen
- ASF (Advanced Systems Format), Wiedergabe von Dateien aus Netzwerkquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8473a2feb4edd567c15d640dfd20e65c2893fe12de6c25a957cc5f730fde0baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027378"
---
# <a name="playing-files-from-a-network-source"></a>Wiederspielen von Dateien aus einer Netzwerkquelle

Das Lesen aus einem Netzwerk ist nicht grundlegend anders als das Lesen einer lokalen Datei. Die Anwendung übergibt die URL an die [**IWMReader::Open-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) des Readerobjekts, und das Readerobjekt verarbeitet die Details der Netzwerkprotokolle. Das Readerobjekt verwendet die intelligente Pufferverwaltung, um eine möglichst reibungslose Wiedergabe zu ermöglichen. Wenn die Anwendung mehr Kontrolle über die Netzwerkeinstellungen des Readerobjekts benötigt, sind diese über [**die Schnittstellen IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) und [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) verfügbar.

Inhalte aus einer Netzwerkquelle fallen in eine der folgenden beiden Kategorien:

-   Streaming. Die Daten werden just-in-time übertragen, um auf dem lokalen Computer abgespielt zu werden. Server mit Windows Media-Dienste können Streamingdaten bereitstellen. Wenn MbR-Inhalte (Multiple Bit Rate) gestreamt werden, kann der Client beim Streaming eine andere Bitrate vom Server anfordern.
-   Heruntergeladen. Alle Daten werden so schnell wie möglich übertragen, sodass sie als Datei auf dem lokalen Computer gespeichert werden können. Webserver stellen heruntergeladene Daten bereit. Es gibt keine Kommunikation zwischen dem Client und dem Server, nachdem der Download begonnen hat.

Wenn das Readerobjekt eine Datei von einem Webserver herunterlädt, wird ein Verfahren namens progressives Streaming verwendet, das es einem Player ermöglicht, mit dem Rendern des Inhalts zu beginnen, bevor der Download abgeschlossen ist. Daten werden gepuffert, um einen ununterbrochenen Datenfluss an den Player zu ermöglichen. Informationen wie Übertragungsrate und Dauer des Inhalts werden verwendet, um zu bestimmen, wie lange die Daten gepuffert werden, bevor sie an den Player übertragen werden.

Um eine Datei oder einen Stream über ein Netzwerk zu öffnen, rufen Sie die **IWMReader::Open-Methode** des Readerobjekts mit der entsprechenden URL auf. **Open** ist ein asynchroner Aufruf, daher wird sofort zurückgegeben. Wenn die Quelle zum Lesen bereit ist, sendet das Readerobjekt eine WMT OPENED-Benachrichtigung an die \_ [**IWMStatusCallback::OnStatus-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) der Anwendung. An diesem Punkt kann die Anwendung den Reader für den Übermittlungsmodus abfragen, indem [**sie IWMReaderAdvanced2::GetPlayMode aufruft.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode) Bei Netzwerkinhalten gibt diese Methode entweder WMT PLAY MODE DOWNLOAD zurück, was auf heruntergeladenen Inhalt hinweist, oder WMT PLAY MODE STREAMING, was auf \_ \_ \_ gestreamten Inhalt \_ \_ \_ hinweist.

Um mit dem Lesen der Datei oder des Streams zu beginnen, rufen Sie [**die IWMReader::Start-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) auf. Der Reader sendet eine WMT BUFFERING START-Benachrichtigung, wenn er mit dem Puffern des Inhalts beginnt, und eine \_ \_ WMT BUFFERING STOP-Benachrichtigung, wenn \_ \_ die Pufferung abgeschlossen ist. Während der Reader Inhalte puffert (d. h. zwischen diesen beiden Benachrichtigungen), sollten Sie den Pufferungsfortschritt für den Benutzer anzeigen. Die [**IWMReaderAdvanced2::GetBufferProgress-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) gibt den Prozentsatz der gepufferten Daten und die geschätzte Zeit zurück, die verbleibt. Für heruntergeladene Inhalte können Sie [**auch IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) aufrufen, um den Downloadfortschritt zu erhalten. Rufen Sie diese Methoden wiederholt auf, um die Anzeige zu aktualisieren, bis die Pufferung abgeschlossen ist. Die Pufferung kann während der Wiedergabe aufgrund von Faktoren wie Netzwerküberlastung erneut auftreten. In diesem Fall erhält die Anwendung eine weitere WMT \_ BUFFERING \_ START-Benachrichtigung.

Wenn das Readerobjekt mit der Wiedergabe des Inhalts beginnt, sendet es eine WMT \_ STARTED-Benachrichtigung. Wenn jedes Beispiel decodiert wird und zum Rendern verfügbar wird, übergibt der Reader es über die [**RÜCKRUFMETHODE IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) an die Anwendung. An diesem Punkt ist der Prozess identisch mit dem für die lokale Dateiwiedergabe. Wenn die Wiedergabe beendet wird, sendet der Reader eine WMT \_ END \_ OF \_ STREAMING-Benachrichtigung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




