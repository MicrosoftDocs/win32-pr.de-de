---
description: Wiedergabe von ASF-Webstream in DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Wiedergabe von ASF-Webstream in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341938"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Wiedergabe von ASF-Webstream in DirectShow

Microsoft DirectShow unterstützt Webstreams in Dateiwiedergabe Szenarios über den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter. Sie müssen jedoch einen eigenen DirectShow-Filter schreiben, um den Stream zu erfassen und beizubehalten.

> [!Note]  
> Um Webstreams in Inhalten wiederzugeben, die von einem Server mit Windows Media Services gestreamt werden, verwenden Sie die Windows Media Player 9-Reihe ActiveX®-Steuerelement, das in eine Webseite eingebettet ist.

 

Wenn eine Datei mit Streams vom Typ "wmmediatype \_ Filetransfer" angegeben wird, erstellt der WM-ASF-Reader eine Ausgabe-PIN. Der Format Block ist eine [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Struktur. (Diese Struktur ist in der Dokumentation zum Windows Media-Format SDK dokumentiert.) Wenn kein downstreamfilter verfügbar ist, mit dem dieser Medientyp verarbeitet werden kann, bleibt die PIN unverändert, aber die Datei findet weiterhin die Audiodaten und/oder Videostreams.

Jedes Medien Beispiel in einem Webstream enthält eine [**WMT- \_ Webstream- \_ Beispiel \_ Header**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) Struktur, die in der Dokumentation zum Windows Media-Format SDK dokumentiert ist. Die-Struktur hat eine Variable Länge, abhängig von der Länge des **wszurl** -Members. Der Zeiger auf die Beispiel Daten zeigt zunächst auf diese-Struktur, und Sie müssen den Zeiger hinter der-Struktur bewegen, um auf die eigentlichen Daten im Stream zuzugreifen.

Der Filter für den webstreamhandler sollte auf der [**cbasererererklasse**](cbaserenderer.md) basieren. In der [**cbaserderderer::D orendersample**](cbaserenderer-dorendersample.md) -Methode muss der Filter die Struktur nach Informationen über den Webstream analysieren und dann die entsprechende Aktion ausführen. In der Regel umfasst dies das Speichern der Datei auf dem Datenträger und das anschließende Aufrufen der Funktionen [**createurlcacheentry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) und [**commiturlcacheentryw**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) oder [**commiturlcacheentrya**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) , um die Dateien in den Internet Explorer-Cache zu platzieren. Der Filter muss mehrteilige Dateien verarbeiten, d. h. Dateien, die größer als ein Beispiel sind, und auch Rendering-Befehle verarbeiten müssen, die vom **WMT- \_ Webstream \_ Sample \_ Header. wsampletype** -Member angegeben werden. Der Filter sendet ein Ereignis für einen [**EC- \_ OLE- \_ Ereignis**](ec-ole-event.md) an die Anwendung zusammen mit dem Text der **WMT- \_ Webstream \_ Sample \_ Header. wszurl** -Zeichenfolge, die den Namen der Datei enthält, die gerendert werden soll. Die Anwendung bewirkt dann, dass der Browser die angegebene Seite anzeigt. Wenn der Webstream ordnungsgemäß erstellt wurde, sollte sich die Datei bereits im Cache befinden.

Weitere Informationen zum WMT \_ -Webstream \_ -Format und zum WMT- \_ Webstream- \_ Beispiel \_ Header finden Sie in der Dokumentation zum Windows Media-Format SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
