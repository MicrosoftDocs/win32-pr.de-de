---
description: Die folgenden GUIDs werden für die Ereignisablaufverfolgung in DirectShow verwendet.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: Ablaufverfolgungs-GUIDs (PerfStruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951549"
---
# <a name="trace-guids"></a>Ablaufverfolgungs-GUIDs

Die folgenden GUIDs werden für die Ereignisablaufverfolgung in DirectShow verwendet.



| GUID                                                                                                                                                                   | Beschreibung                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | Audiopausenereignis. Ereignisse dieses Typs verwenden die [**PERFINFO \_ DSHOW \_ AUDIOBREAK-Struktur**](perfinfo-dshow-audiobreak.md) für Ereignisdaten.<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**GUID \_ DSHOW \_ CTL**</dt> </dl>      | DirectShow-Ereignisanbieter.<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | Allgemeines Streamingereignis. Ereignisse dieses Typs verwenden die [**PERFINFO \_ DSHOW \_ STREAMTRACE-Struktur**](perfinfo-dshow-streamtrace.md) für Ereignisdaten.<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | Videorenderingereignis. Ereignisse dieses Typs verwenden die [**PERFINFO \_ \_ DSHOW-APROTOKOLLND-Struktur**](perfinfo-dshow-avrend.md) für Ereignisdaten.<br/>             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PerfStruct.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisablaufverfolgung in DirectShow](event-tracing-in-directshow.md)
</dt> </dl>

 

 




