---
description: Gibt an, ob der Alpha Modus für Farb Medien-Video Typen vorab multipliziert oder gerade ist.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042339"
---
# <a name="mf_mt_alpha_mode-attribute"></a>MF- \_ MT- \_ Alpha Mode- \_ Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Gibt an, ob der Alpha Modus für Farb Medien-Video Typen vorab multipliziert oder gerade ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieser Wert kann in einen Wert für den [**DXGI- \_ alpha \_ Modus**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) umgewandelt werden. Wenn dieses Attribut nicht vorhanden ist, ist der Wert aus Gründen der Abwärtskompatibilität der **DXGI- \_ alpha- \_ Modus \_ direkt** für das Videoformat, der Alphakanal unterstützt, z. b. ARGB32, oder der **DXGI- \_ alpha \_ Modus \_ Ignore** für das Videoformat ohne Alphakanal, z. b.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
