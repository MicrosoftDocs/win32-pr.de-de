---
title: Schreiben komprimierter Beispiele
description: Schreiben komprimierter Beispiele
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), Schreiben komprimierter Beispiele
- ASF (Advanced Systems Format), Schreiben komprimierter Beispiele
- Advanced Systems Format (ASF), Übergeben komprimierter Beispiele
- ASF (Advanced Systems Format), Übergeben komprimierter Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa6bf5298e465716fe7a60eb5de2459f09be405611ac7322b534804bbbc997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843654"
---
# <a name="writing-compressed-samples"></a>Schreiben komprimierter Beispiele

Bei einigen Audio- oder Videostreams sollten Sie Beispiele übergeben, die bereits komprimiert sind, anstatt Rohdaten zu übergeben. Dieses Feature wird verwendet, um einen vorhandenen Stream zu kopieren oder Mit einem Drittanbietercodec komprimierte Beispiele zu schreiben. Der Prozess des Schreibens eines komprimierten Beispiels ist identisch mit dem Schreiben eines nicht komprimierten Beispiels, mit der Ausnahme, dass Sie [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anstelle von [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)verwenden. Weitere Informationen zum Schreiben von nicht komprimierten Beispielen finden Sie unter [So schreiben Sie Beispiele.](to-write-samples.md)

Wenn Sie komprimierte Beispiele für CBR-Profile schreiben, werden vom Writer ggf. einige Stichproben abgelegt, um den Inhalt innerhalb der angegebenen Bitrate und der Pufferfensterwerte zu halten. Für VBR werden vom Writer keine Stichproben abgelegt, aber es gibt keine Möglichkeit, sicherzustellen, dass die Bitrate und die Pufferfensterwerte korrekt sind.

Wenn Sie einen Stream aus einer Datei in eine andere kopieren, sollten Sie immer das Streamkonfigurationsobjekt aus dem Profil der ursprünglichen Datei in das Profil der neuen Datei kopieren. Dadurch wird sichergestellt, dass Sie über die richtige Bitrate und die richtigen Pufferfensterinformationen verfügen. Wenn Sie einen komprimierten Stream in einen Stream kopieren, für den ein niedrigeres Pufferfenster festgelegt ist, werden die Beispiele beim Schreiben von Dateien gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




