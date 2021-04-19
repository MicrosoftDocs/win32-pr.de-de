---
description: Ein Wert, der angibt, ob ein Frame mithilfe der aktiven Infrarotbeleuchtung (IR) erfasst wurde.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348811"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>MF- \_ Attribut zur Erfassung von \_ \_ metadatenframe \_

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein Wert, der angibt, ob ein Frame mithilfe der aktiven Infrarotbeleuchtung (IR) erfasst wurde.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist eine Bitmaske. Es handelt sich um einen 64-Bit-Wert für die Abwärtskompatibilität.

Die aktive Beleuchtung ist, wenn ein Gerät einen Licht Emitter hat, der sich in der Nähe der IR-Kamera befindet und einen Lichtstrahl ausgibt, um die Szene zu beleuchten Legen Sie Value auf (Wert & 0x1)! = 0 fest, wenn Frame aufgezeichnet wurde, als die aktive Beleuchtung aktiviert war, und legen Sie (Wert & 0x1) = = 0 fest, wenn die aktive Beleuchtung deaktiviert war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




