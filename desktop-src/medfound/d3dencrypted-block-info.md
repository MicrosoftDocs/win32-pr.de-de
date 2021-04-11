---
description: Gibt an, welche Bytes in einer geschützten Video Oberfläche verschlüsselt werden.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127917"
---
# <a name="d3dencrypted_block_info-structure"></a>D3DENCRYPTED \_ Block \_ Info-Struktur

Gibt an, welche Bytes in einer geschützten Video Oberfläche verschlüsselt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Numverschlüsseltedbytesatstart**
</dt> <dd>

Die Anzahl der Bytes, die am Anfang des Puffers verschlüsselt werden.

</dd> <dt>

**Numbytesinskippattern**
</dt> <dd>

Die Anzahl der Bytes, die nach den ersten **numverschlüsseltedbytesatbeginungsbytes** übersprungen werden, und dann nach jedem Block von **numbytesinverschlüsseltpattern** -bytes. Übersprungene Bytes werden nicht verschlüsselt.

</dd> <dt>

**Numbytesinverschlüsseltpattern**
</dt> <dd>

Die Anzahl der Bytes, die nach jedem Block von übersprungenen Bytes verschlüsselt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (Include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> </dl>

 

 




