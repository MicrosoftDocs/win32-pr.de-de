---
description: ASF-Webstreamwiedergabe in DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: ASF-Webstreamwiedergabe in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28d9d3b7ea4fba5537383a846e6eff64f3815eefa21613c6056a15a5e497f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824625"
---
# <a name="asf-web-stream-playback-in-directshow"></a>ASF-Webstreamwiedergabe in DirectShow

Microsoft DirectShow unterstützt Webstreams in Dateiwiedergabeszenarien über den [WM ASF-Readerfilter.](wm-asf-reader-filter.md) Sie müssen jedoch einen eigenen DirectShow-Filter schreiben, um den Stream zu erfassen und dauerhaft zu speichern.

> [!Note]  
> Um Webstreams in Inhalten wieder anzuzeigen, die von einem Server gestreamt werden, auf dem Windows Media-Dienste ausgeführt wird, verwenden Sie das Windows Media Player 9 Series ActiveX®-Steuerelement, das in eine Webseite eingebettet ist.

 

Wenn eine Datei mit Streams vom Typ WMMEDIATYPE FileTransfer angegeben wird, erstellt der \_ WM ASF-Reader einen Ausgabepin dafür. Der Formatblock ist eine [**WMT \_ WEBSTREAM \_ FORMAT-Struktur.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) (Diese Struktur ist in der Dokumentation zum Windows Media Format SDK dokumentiert.) Wenn kein Downstreamfilter verfügbar ist, der diesen Medientyp verarbeiten kann, bleibt der Pin nicht verbunden, aber die Datei gibt weiterhin die Audio- und/oder Videostreams wieder.

Jedes Medienbeispiel in einem Webstream enthält eine [**WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER-Struktur,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) die in der Dokumentation Windows Media Format SDK dokumentiert ist. Die -Struktur hat eine variable Länge, die von der Länge ihres **wszURL-Members** abhängig ist. Der Zeiger auf die Beispieldaten zeigt anfänglich auf diese Struktur, und Sie müssen den Zeiger über die Struktur hinaus steigern, um auf die tatsächlichen Daten im Stream zu zugreifen.

Der Webstreamhandlerfilter sollte auf der [**CBaseRenderer-Klasse**](cbaserenderer.md) basieren. In [**der CBaseRenderer::D oRenderSample-Methode**](cbaserenderer-dorendersample.md) muss der Filter die Struktur auf Informationen zum Webstream analysieren und dann die entsprechende Aktion ausführen. In der Regel umfasst dies das Speichern der Datei auf dem Datenträger und das anschließende Aufrufen der [**Funktionen CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) und [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) oder [**CommitUrlCacheEntryA,**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) um die Dateien im Internet Explorer-Cache zu speichern. Der Filter muss mehrteilige Dateien verarbeiten, d. h. Dateien, die größer als ein Beispiel sind, sowie Renderbefehle verarbeiten, die vom **WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER.wSampleType-Member** angegeben werden. Der Filter sendet ein [**EC \_ OLE \_ EVENT-Ereignis**](ec-ole-event.md) zusammen mit dem Text der **WMT \_ WEBSTREAM SAMPLE \_ \_ HEADER.wszURL-Zeichenfolge,** die den Namen der zu renderenden Datei enthält, an die Anwendung. Die Anwendung bewirkt dann, dass im Browser die angegebene Seite angezeigt wird. Wenn der Webstream ordnungsgemäß geschrieben wurde, sollte die Datei bereits im Cache vorhanden sein.

Weitere Informationen zu WMT \_ WEBSTREAM FORMAT und WMT WEBSTREAM SAMPLE HEADER finden Sie in der Dokumentation Windows \_ \_ Media Format \_ \_ SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
