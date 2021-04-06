---
title: Verwenden des Kontext Parameters
description: Verwenden des Kontext Parameters
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media-Format-SDK, Kontext Parameter
- Windows Media-Format-SDK, pvcontext-Parameter
- pvcontext-Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101242"
---
# <a name="using-the-context-parameter"></a>Verwenden des Kontext Parameters

Einige der vom Windows Media Format SDK verwendeten Rückrufe akzeptieren einen Parameter namens *pvcontext*. Die aufrufenden Objekte übergeben den Wert, den Sie in der Methode angeben, die mit der asynchronen Aktion begonnen hat. Wenn Sie z. b. [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)aufgerufen haben, können Sie einen Wert für *pvcontext* übergeben. Wenn die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode vom Reader-Objekt aufgerufen wird, um die Anwendung zu benachrichtigen, dass die Datei geöffnet wurde, übergibt Sie den Wert, den Sie in Ihrem Aufruf zum **Öffnen** als *pvcontext* -Parameter von **OnStatus** verwendet haben. Dieser Kontext Parameter wird für ihre Verwendung bereitgestellt und kann in beliebiger Weise verwendet werden.

Der *pvcontext* -Parameter wird am häufigsten verwendet, wenn mehrere Objekte denselben Rückruf gemeinsam verwenden müssen. Mehrere-Objekte verwenden z. b. die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode. Sie können *pvcontext* verwenden, damit die verschiedenen Objekte eine Implementierung von **OnStatus** freigeben können, indem Sie einen anderen Wert für *pvcontext* für den ursprünglichen-Befehl übergeben. In ihrer Implementierung von **OnStatus** können Sie die Logik zur Verarbeitung von Nachrichten basierend auf dem Wert von *pvcontext* verzweigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückruf Methoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




