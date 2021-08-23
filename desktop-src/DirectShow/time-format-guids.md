---
description: Die folgenden GUIDs (Globally Unique Identifiers) definieren verschiedene Zeitformate.
ms.assetid: 510c7146-ff3c-4812-a7ad-b4051aa82ef3
title: Zeitformat-GUIDs (Uuids.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd12f9c460f0874845a2b323975f577631f9d99abf2e2d654b21c2a2b0824e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951699"
---
# <a name="time-format-guids"></a>Zeitformat-GUIDs

Die folgenden GUIDs (Globally Unique Identifiers) definieren verschiedene Zeitformate.



| GUID                                                                                                                                                                                       | Beschreibung                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="TIME_FORMAT_NONE"></span><span id="time_format_none"></span><dl> <dt>**ZEITFORMAT \_ \_ KEINE**</dt> </dl>                    | Kein Format.<br/>                             |
| <span id="TIME_FORMAT_FRAME"></span><span id="time_format_frame"></span><dl> <dt>**\_ \_ ZEITFORMATRAHMEN**</dt> </dl>                 | Videoframes.<br/>                          |
| <span id="TIME_FORMAT_SAMPLE"></span><span id="time_format_sample"></span><dl> <dt>**\_ \_ ZEITFORMATBEISPIEL**</dt> </dl>              | Beispiele im Stream.<br/>                 |
| <span id="TIME_FORMAT_FIELD"></span><span id="time_format_field"></span><dl> <dt>**\_ \_ ZEITFORMATFELD**</dt> </dl>                 | Verschachtelte Videofelder.<br/>               |
| <span id="TIME_FORMAT_BYTE"></span><span id="time_format_byte"></span><dl> <dt>**TIME \_ FORMAT \_ BYTE**</dt> </dl>                    | Byteoffset im Stream.<br/>         |
| <span id="TIME_FORMAT_MEDIA_TIME"></span><span id="time_format_media_time"></span><dl> <dt>**\_ZEITFORMAT \_ \_ MEDIENZEIT**</dt> </dl> | Referenzzeit (Einheiten von 100 Nanosekunden).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Uuids.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
</dt> </dl>

 

 




