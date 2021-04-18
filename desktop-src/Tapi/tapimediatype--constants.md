---
description: Die Medientyp Konstanten sind unten definiert.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ Konstanten (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371281"
---
# <a name="tapimediatype_-constants"></a>Tapimediatype- \_ Konstanten

Die folgenden Medientypen sind definiert:



| Konstante/Wert                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**Tapimediatype \_ Audiodatei**</dt> <dt>0x8</dt> </dl>                    | Ein audiomedienstream, der den Computer eingibt oder verlässt. Ein Eingabestream wird in der Regel auf Referenten abgespielt oder an ein Mobilgerät gesendet, und ein verlässt Stream wird in der Regel über ein Mikrofon oder Mobilgerät erfasst.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**Tapimediatype \_ Video**</dt> <dt>0X8000</dt> </dl>                 | Ein Video Mediendaten Strom, der den Computer eingibt oder verlässt. Ein Eingabestream wird in der Regel in einem Videofenster gerendert, und ein belassen von Mediendaten wird normalerweise mit einer Videokamera aufgezeichnet.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**Tapimediatype \_ DataModem**</dt> <dt>0x10</dt> </dl>       | Ein Daten Mediendaten Strom, der einem Datenmodem zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**Tapimediatype \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Ein Daten Mediendaten Strom, der einem G3-Protokoll Fax zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**Tapimediatype \_ Multitrack**</dt> <dt>0x10000</dt> </dl> | Ein Stream befindet sich in einem Multitrack-Terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**\_Einzelner RTP- \_ Stream für MediaType \_**</dt> </dl>     | Diese GUID wird zwischen einem von der Anwendung bereitgestellten Terminal und dem MSP-Stream verwendet. Wenn die PIN des Terminals diesen Medientyp unterstützt, tauscht der Stream unformatierte RTP-Daten mit dem Terminal aus. Dieser Modus wird nur von den Videostreams in h323 MSP und ipconf MSP für Windows 2000 SP1 oder höher unterstützt.<br/> **Header:** In "ipmsp. h" deklariert. Der Header "ipmsp. h" ist in unter Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                              |
| Header<br/>       | <dl> <dt>Tapi3. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itqoabvent:: get- \_ mediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**Itammediaformat:: get \_ Mediaformat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**Itammediaformat::p UT \_ Mediaformat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**Itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**Itmediasupport:: get- \_ mediatypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**Itterminalsupport:: "kreateterminal"**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

