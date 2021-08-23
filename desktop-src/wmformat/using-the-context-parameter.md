---
title: Verwenden des Kontextparameters
description: Verwenden des Kontextparameters
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Medienformat-SDK, Kontextparameter
- Windows Media Format SDK, pvContext-Parameter
- pvContext-Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585200"
---
# <a name="using-the-context-parameter"></a>Verwenden des Kontextparameters

Einige der Rückrufe, die vom Windows Media Format SDK verwendet werden, verwenden einen Parameter namens *pvContext.* Die aufrufenden Objekte übergeben den Wert, den Sie in der Methode angeben, die die asynchrone Aktion gestartet hat. Wenn Sie beispielsweise [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)aufrufen, können Sie einen Wert für *pvContext* übergeben. Wenn die [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) vom Readerobjekt aufgerufen wird, um Ihre Anwendung zu benachrichtigen, dass die Datei geöffnet wurde, übergibt sie den Wert, den Sie in Ihrem Aufruf von **Open** als *pvContext-Parameter* von **OnStatus** verwendet haben. Dieser Kontextparameter wird für Ihre Verwendung bereitgestellt, und Sie können ihn auf beliebige Weise verwenden.

Der *pvContext-Parameter* wird am häufigsten verwendet, wenn mehrere Objekte denselben Rückruf verwenden müssen. Beispielsweise verwenden mehrere Objekte die [**IWMStatusCallback::OnStatus-Methode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Sie können *pvContext* verwenden, um den verschiedenen Objekten zu ermöglichen, eine Implementierung von **OnStatus** gemeinsam zu nutzen, indem Sie einen anderen Wert für *pvContext* bei Ihrem ursprünglichen Aufruf übergeben. In Ihrer Implementierung von **OnStatus** können Sie die Nachrichtenverarbeitungslogik basierend auf dem Wert von *pvContext* verzweigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückrufmethoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




