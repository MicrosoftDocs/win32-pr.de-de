---
description: Ein -Wert, der angibt, ob ein Frame mithilfe eines aktiven Ir-Schildes (ActiveIra) erfasst wurde.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23658f8f396a81180a074badc43e98d0f392fc355c1a81a4d1e731d132de12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973949"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>MF \_ CAPTURE METADATA FRAME \_ \_ \_ FRAME-Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein -Wert, der angibt, ob ein Frame mithilfe eines aktiven Ir-Schildes (ActiveIra) erfasst wurde.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist eine Bitmaske. Aus Gründen der Abwärtskompatibilität ist dies ein 64-Bit-Wert.

Aktives Licht ist, wenn ein Gerät einen Lichtausträger in der Nähe der IR-Kamera hat, der einen Lichtstrahl aussendet, um die Szene zu beleuchten. In der Regel wird IR-Licht ausgegeben, sodass es keine menschlichen Augen beeinträchtigt. Legen Sie den Wert auf (Wert & 0x1) != 0 fest, wenn der Frame erfasst wurde, als aktives Licht eingeschaltet war, und legen Sie (Wert & 0x1) == 0 fest, wenn aktives Licht ausgeschaltet war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




