---
title: Anhalten oder Anhalten der Wiedergabe
description: Anhalten oder Anhalten der Wiedergabe
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), Anhalten der Wiedergabe
- ASF (Advanced Systems Format), Anhalten der Wiedergabe
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Beenden der Wiedergabe
- ASF (Advanced Systems Format), Beenden der Wiedergabe
- Advanced Systems Format (ASF), Wiedergabe anhalten oder beenden
- ASF (Advanced Systems Format), Wiedergabe wird angehalten oder angehalten
- asynchrone Reader, Anhalten der Wiedergabe
- asynchrone Lesevorgänge, Beenden der Wiedergabe
- asynchrone Leser, Wiedergabe wird angehalten oder angehalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516598"
---
# <a name="to-pause-or-stop-playback"></a>Anhalten oder Anhalten der Wiedergabe

Wenn Sie [**iwmreader:: Start starten**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) , um mit der Wiedergabe einer Datei zu beginnen, wird der asynchrone Reader mit der Verarbeitung in seinen eigenen separaten Threads fortgesetzt, bis das Ende der Datei erreicht ist. Sie können die Übermittlung von Beispielen mithilfe der [**iwmreader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) -Methode oder der [**iwmreader::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) anhaltemethode anhalten oder stoppen.

## <a name="pausing"></a>Status „Wird angehalten“

Wenn Sie **iwmreader::P ause** aufzurufen, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader die aktuelle Position in der Datei. Um die Wiedergabe nach dem Anhalten fortzusetzen, nennen Sie [**iwmreader:: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume). Die Wiedergabe wird an dem Punkt fortgesetzt, an dem Sie angehalten wurde.

## <a name="stopping"></a>Wird beendet

Wenn Sie **iwmreader:: Stop** aufgerufen haben, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader keine Informationen über den Fortschritt der Wiedergabe. Wenn Sie " **Stop** " und höher verwenden möchten, müssen Sie die Präsentationszeit des letzten übermittelten Beispiels speichern und in Ihrem Aufruf von " **iwmreader:: Start**" verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




