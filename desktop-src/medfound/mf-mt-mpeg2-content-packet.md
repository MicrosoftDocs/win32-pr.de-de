---
description: Bei einem Medientyp, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, wird angegeben, ob die Transport Pakete Inhalts Paket Header enthalten.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: MF_MT_MPEG2_CONTENT_PACKET-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866572"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>Paket "MF \_ MT \_ MPEG2 \_ Content \_ Packet"

Bei einem Medientyp, der einen MPEG-2-Transportdaten Strom (TS) beschreibt, wird angegeben, ob die Transport Pakete Inhalts Paket Header enthalten.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                                                | Bedeutung                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Es werden keine Inhalts Paket Header hinzugefügt.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Bei Intervallen von 200 – 1000 Millisekunden wird dem Anfang des Transport Pakets eine 14-Byte-Inhalts Paket Kopfzeile hinzugefügt, wie durch die Zuordnung von Radio Industrie und Unternehmen (ARIB) Standard definiert.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




