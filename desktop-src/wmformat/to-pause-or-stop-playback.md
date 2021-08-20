---
title: So halten Sie die Wiedergabe an oder beenden sie
description: So halten Sie die Wiedergabe an oder beenden sie
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), Anhalten der Wiedergabe
- ASF (Advanced Systems Format), Anhalten der Wiedergabe
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), Beenden der Wiedergabe
- ASF (Advanced Systems Format), Beenden der Wiedergabe
- Advanced Systems Format (ASF), Anhalten oder Beenden der Wiedergabe
- ASF (Advanced Systems Format), Anhalten oder Beenden der Wiedergabe
- asynchrone Reader, Anhalten der Wiedergabe
- asynchrone Reader, Beenden der Wiedergabe
- asynchrone Reader, Anhalten oder Beenden der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7ae7f3c1dd2c045a35b8d3ee8950ace849a032136371f9da7ff1bcc2b12de27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845365"
---
# <a name="to-pause-or-stop-playback"></a>So halten Sie die Wiedergabe an oder beenden sie

Wenn Sie [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) aufrufen, um mit der Wiedergabe einer Datei zu beginnen, setzt der asynchrone Reader die Verarbeitung in eigenen separaten Threads fort, bis das Ende der Datei erreicht ist. Sie können die Übermittlung von Beispielen mithilfe der Methoden [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) bzw. [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) anhalten oder beenden.

## <a name="pausing"></a>Status „Wird angehalten“

Wenn Sie **IWMReader::P ause** aufrufen, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader die aktuelle Position in der Datei. Um die Wiedergabe nach dem Anhalten fortzusetzen, rufen [**Sie IWMReader::Resume auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume) Die Wiedergabe wird ab dem Zeitpunkt fortgesetzt, an dem sie angehalten wurde.

## <a name="stopping"></a>Wird beendet

Wenn Sie **IWMReader::Stop** aufrufen, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader keine Informationen zum Fortschritt der Wiedergabe. Um **Stop** zu verwenden und später zum Beendigungspunkt zurückzukehren, müssen Sie die Präsentationszeit des letzten übermittelten Beispiels speichern und in Ihrem Aufruf von **IWMReader::Start** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




