---
title: Webstream-Wiedergabe in DirectShow
description: Webstream-Wiedergabe in DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Webstream-Wiedergabe
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Wiedergabe von Webstreams
- ASF (Advanced Systems Format), Webstream-Wiedergabe
- DirectShow, Webstream-Wiedergabe
- Webstreams, DirectShow
- Webstreams, Wiedergabe in DirectShow
- Streams, Webstream-Wiedergabe in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947537"
---
# <a name="web-stream-playback-in-directshow"></a>Webstream-Wiedergabe in DirectShow

Microsoft DirectShow unterstützt Webstreams (Weitere Informationen finden Sie unter [Webstreams](web-streams.md) ) in Dateiwiedergabe Szenarios über den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter. Sie müssen jedoch einen eigenen DirectShow-Filter schreiben, um den Stream zu erfassen und beizubehalten.

> [!Note]  
> Um Webstreams in Inhalten wiederzugeben, die von einem Server mit Windows Media Services gestreamt werden, verwenden Sie die Windows Media Player 9-Reihe ActiveX®-Steuerelement, das in eine Webseite eingebettet ist.

 

Wenn eine Datei mit Streams vom Typ "wmmediatype \_ Filetransfer" angegeben wird, erstellt der WM-ASF-Reader eine Ausgabe-PIN. Der Format Block ist eine [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Struktur. Wenn kein downstreamfilter verfügbar ist, mit dem dieser Medientyp verarbeitet werden kann, bleibt die PIN unverändert, aber die Datei findet weiterhin die Audiodaten und/oder Videostreams.

Es ist wichtig zu verstehen, dass jedes Medien Beispiel in einem Webstream eine [**WMT- \_ Webstream- \_ Beispiel \_ Header**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) Struktur enthält, die abhängig von der Länge des **wszurl** -Members eine Variable Länge aufweist. Der Zeiger auf die Beispiel Daten zeigt zunächst auf diese-Struktur, und Sie müssen den Zeiger hinter der-Struktur bewegen, um auf die eigentlichen Daten im Stream zuzugreifen. Der Filter für den webstreamhandler sollte auf der **cbasererererklasse** basieren. In der Methode " **dorendersample** " muss der Filter die Struktur nach Informationen über den Webstream analysieren und dann die entsprechende Aktion ausführen. In der Regel umfasst dies das Speichern der Datei auf dem Datenträger und das anschließende Aufrufen von " **commiturlcacheentry** " und " **createurlcacheentry** ", um die Dateien in den Internet Explorer-Cache zu platzieren. Der Filter muss mehrteilige Dateien verarbeiten, d. h. Dateien, die größer als ein Beispiel sind, und auch Rendering-Befehle verarbeiten müssen, die vom **WMT- \_ Webstream \_ Sample \_ Header. wsampletype** -Member angegeben werden. Der Filter sendet ein **EC- \_ OLE- \_ Ereignis** zusammen mit dem Text der **WMT- \_ Webstream- \_ Beispiel \_ Kopfzeile. wszurl** -Zeichenfolge, die den Namen der Datei enthält, die gerendert werden soll. Die Anwendung bewirkt dann, dass der Browser die angegebene Seite anzeigt. Wenn der Webstream ordnungsgemäß erstellt wurde, sollte sich die Datei bereits im Cache befinden.

Weitere Informationen zu **cbaserderderer**, **dorendersample** und **EC \_ OLE \_ Event** finden Sie in der DirectShow SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Webstreams**](web-streams.md)
</dt> </dl>

 

 




