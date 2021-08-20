---
description: Gibt an, welche Bytes in einer geschützten Videooberfläche verschlüsselt werden.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO-Struktur (D3d9types.h)
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
ms.openlocfilehash: 94027dac3956376e32ad10cf7c1b600d9c65f3918e2781ab9da96d4d3891f43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879724"
---
# <a name="d3dencrypted_block_info-structure"></a>D3DENCRYPTED \_ BLOCK \_ INFO-Struktur

Gibt an, welche Bytes in einer geschützten Videooberfläche verschlüsselt werden.

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

**NumEncryptedBytesAtBeginning**
</dt> <dd>

Die Anzahl der Bytes, die am Anfang des Puffers verschlüsselt werden.

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

Die Anzahl der Bytes, die nach den ersten **NumEncryptedBytesAtBeginning-Bytes** und dann nach jedem Block von **NumBytesInEncryptPattern-Bytes** übersprungen werden. Übersprungene Bytes werden nicht verschlüsselt.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Die Anzahl der Bytes, die nach jedem Block übersprungener Bytes verschlüsselt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (einschließlich D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> </dl>

 

 




