---
description: Dieser Filter demultiplexiert MPEG-2-Transport- und Programmstreams, die im Pushmodus übermittelt werden.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2-Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983953"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2-Demultiplexer

Dieser Filter demultiplexiert MPEG-2-Transport- und Programmstreams, die im Pushmodus übermittelt werden. Ab Windows XP unterstützt dieser Filter auch Programmstreams im Pullmodus (Dateiwiedergabe). Verwenden Sie auf früheren Plattformen den [MPEG-2-Splitter-Filter](mpeg-2-splitter.md) für Programmstreams im Pullmodus. Dieser Filter kann in jeder Art von Filterdiagramm verwendet werden, einschließlich eines BDA-Digital TV-Filterdiagramms.

> [!Note]  
> Der MPEG-2-Demultiplexer unterstützt keine framegenauen Sucher.

 




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | Alle Modi:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><strong>Ispecifypropertypages</strong></li></ul>Nur Pushmodus:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Eingabepin-Medientypen | Haupttyp: MEDIATYPE_STREAM<br /> Untertyp:<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2-Demultiplexer-Medientypen.</strong></a><br /> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | Elementare Audio- und Videostreams müssen einen Haupttyp MEDIATYPE_Audio oder MEDIATYPE_Video.<br /> Weitere Informationen finden Sie unter <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2-Demultiplexer-Medientypen.</strong></a><br /> | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>nur IQualityControl-Pushmodus:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource,</strong></a> <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Nur Pullmodus: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | 
| Filtern der CLSID | CLSID_MPEG2Demultiplexer | 
| Eigenschaftenseite CLSID | Nur zum Testen verfügbar. Verwenden der <strong>ISpecifyPropertyPages-Schnittstelle</strong> für den Zugriff auf die Eigenschaftenseiten | 
| Ausführbare Datei | mpg2splt.ax | 
| <a href="merit.md">Verdienst</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Bemerkungen

Zum Ausgabe von elementaren Audio- und Videostreams muss demux die PCR- und SCR-Streams empfangen. Auf der Eingabeseite bedeutet dies, dass ein Transportstream die PAT- und PMT-Tabellen enthalten muss, die die PID für den PCR-Stream definieren. und Programmstreams müssen mindestens einen Paketheader enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |
| Ende des Supports (Server)<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




