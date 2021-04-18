---
description: Ein-Wert, der den Typ des Sensors angibt, der von einer Frame Quelle bereitgestellt wird, z. b. Farbe, Infrarot oder Tiefe.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343779"
---
# <a name="mf_mt_framesource_types-attribute"></a>Attribut "MF \_ MT \_ framesource \_ types"

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ein-Wert, der den Typ des Sensors angibt, der von einer Frame Quelle bereitgestellt wird, z. b. Farbe, Infrarot oder Tiefe.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieser Wert muss ein Member der [**\_ mfframesourcetypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) -Enumeration sein. Wenn dieses Attribut nicht für einen Medientyp definiert ist, wird aus Gründen der Abwärtskompatibilität angenommen, dass es **\_ mfframesourcetyes:: Color** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
