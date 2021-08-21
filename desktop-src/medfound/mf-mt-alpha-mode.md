---
description: Gibt an, ob der Alphamodus für Farbmedienvideotypen prämultiplizierend oder gerade ist.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c658cae64c68aa89c49230164707d75369c021767c6aa0b46818516ffa26513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035318"
---
# <a name="mf_mt_alpha_mode-attribute"></a>MF \_ MT \_ ALPHA \_ MODE-Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Gibt an, ob der Alphamodus für Farbmedienvideotypen prämultiplizierend oder gerade ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieser Wert kann in einen [**DXGI \_ ALPHA \_ MODE-Wert**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) umgeschaltet werden. Wenn dieses Attribut nicht vorhanden ist, lautet der Wert aus Gründen der Abwärtskompatibilität **DXGI \_ ALPHA MODE \_ \_ STRAIGHT** für das Videoformat, das den Alphakanal unterstützt, z. B. ARGB32, oder **DXGI ALPHA MODE \_ \_ \_ IGNORE** für das Videoformat ohne Alphakanal, z. B. RGB32.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
