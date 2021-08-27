---
description: Ein -Wert, der den Typ des Sensors angibt, der von einer Framequelle bereitgestellt wird, z. B. Farbe, Lichtfarbe oder Tiefe.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3cddc28db050ec3fdb55e47ca2ceb1bd24fb2813bdf90fce439843957a7ae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113770"
---
# <a name="mf_mt_framesource_types-attribute"></a>MF \_ MT \_ FRAMESOURCE \_ TYPES-Attribut

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein -Wert, der den Typ des Sensors angibt, der von einer Framequelle bereitgestellt wird, z. B. Farbe, Lichtfarbe oder Tiefe.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieser Wert sollte ein Member der [**\_ MFFrameSourceTypes-Enumeration**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) sein. Aus Gründen der Abwärtskompatibilität wird angenommen, dass dieses Attribut **\_ MFFrameSourceTyes::Color** ist, wenn es nicht für einen Medientyp definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
