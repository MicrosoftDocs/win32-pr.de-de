---
description: Die Medientypkonstanten sind unten definiert.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ Konstanten (Tapi3.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a702f5a061629f3fd8daa5ad742c65af12c43bbd92eec6896b143e4bd6a403c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866880"
---
# <a name="tapimediatype_-constants"></a>TAPIMEDIATYPE-Konstanten \_

Die folgenden Medientypen sind definiert:



| Konstante/Wert                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt> </dl>                    | Ein Audiomedienstream, der den Computer ein- oder verlässt. Ein eingeschalteter Mediendatenstrom wird in der Regel auf Lautsprechern wiedergegeben oder an ein Handsetgerät gesendet, und ein verlassener Datenstrom wird in der Regel über ein Mikrofon oder ein Gerät erfasst.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ VIDEO**</dt> <dt>0x8000</dt> </dl>                 | Ein Videomedienstream, der den Computer ein- oder verlässt. Ein medieneingabeender Datenstrom wird in der Regel in einem Videofenster gerendert, und ein verlassener Medienstream wird in der Regel mit einer Videokamera erfasst.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ DATAMODEM-0x10**</dt> <dt></dt> </dl>       | Ein Datenmedienstream, der einem Datenmodem zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX-0x20**</dt> <dt></dt> </dl>                   | Ein Datenmedienstream, der einem G3-Protokollfax zugeordnet ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ MULTITRACK**</dt> <dt>0x10000</dt> </dl> | Ein Stream befindet sich in einem Terminal mit mehreren Nachverfolgungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**MEDIATYPE \_ RTP \_ Single \_ Stream**</dt> </dl>     | Diese GUID wird zwischen einem von der Anwendung bereitgestellten Terminal und dem Datenstrom des MSP verwendet. Wenn der Pin des Terminals diesen Medientyp unterstützt, tauscht der Stream RTP-Rohdaten mit dem Terminal aus. Dieser Modus wird nur von den Videostreams auf dem H323 MSP und IPConf MSP für Windows 2000 SP1 oder höher unterstützt.<br/> **Header:** Deklariert in ipmsp.h. Der Header ipmsp.h ist in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                              |
| Header<br/>       | <dl> <dt>Tapi3.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITQOSEvent::get \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat::get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::put \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport::get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

