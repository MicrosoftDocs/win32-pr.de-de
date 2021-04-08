---
title: So rufen Sie Medien Beispiele mit dem asynchronen Reader ab
description: So rufen Sie Medien Beispiele mit dem asynchronen Reader ab
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Advanced Systems Format (ASF), Abrufen von Medien Beispielen
- ASF (Advanced Systems Format), Abrufen von Medien Beispielen
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Abrufen von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038541"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>So rufen Sie Medien Beispiele mit dem asynchronen Reader ab

Nachdem Sie die WMT- \_ Statusmeldung "geöffnet" in ihrer Implementierung von " [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)" erhalten haben, können Sie mit dem Empfang von Beispielen beginnen, indem Sie [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)aufrufen. Der asynchrone Reader stellt Beispiele für Ihre Implementierung von [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)bereit. Beispiele werden in der Präsentationszeit bereitgestellt.

**Start** ist ein asynchroner-Befehl. Es wird fast sofort zurückgegeben und weiterhin in separaten Threads ausgeführt. Der asynchrone Reader verwendet beim Decodieren von Inhalten und Bereitstellung von Beispielen mehrere Threads. Wenn das Ende der Datei erreicht ist, sendet der Reader eine WMT \_ EOF-Statusmeldung an die Implementierung des **OnStatus** -Rückrufs. Wenn WMT \_ EOF gesendet wird, beendet der Reader seine eigene Verarbeitung. Sie müssen nicht auf WMT \_ EOF mit einem [**callmreader:: Stopp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop)-Befehl reagieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**So implementieren Sie readernachrichten im OnStatus-Rückruf**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**So implementieren Sie den onsample-Rückruf**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




