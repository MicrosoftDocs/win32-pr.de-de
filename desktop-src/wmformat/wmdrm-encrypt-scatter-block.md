---
title: WMDRM_ENCRYPT_SCATTER_BLOCK-Struktur (Wmdrmsdk.h)
description: Die WMDRM \_ ENCRYPT \_ SCATTER \_ BLOCK-Struktur enthält einen Zu verschlüsselnden Datenblock.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK Strukturfenster Medienformat
- Strukturfenster Medienformat
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658160"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>WMDRM \_ ENCRYPT \_ SCATTER \_ BLOCK-Struktur

Die **WMDRM \_ ENCRYPT SCATTER \_ \_ BLOCK-Struktur** enthält einen Zu verschlüsselnden Datenblock.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwStreamID**
</dt> <dd>

Bezeichner des Streams, zu dem der Datenblock gehört.

</dd> <dt>

**cbBlock**
</dt> <dd>

Größe des Blocks in Bytes.

</dd> <dt>

**pbBlock**
</dt> <dd>

Zeiger auf einen Puffer, der den Datenblock enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von der [**IWMDRMEncryptScatter::EncryptScatter-Methode**](iwmdrmencryptscatter-encryptscatter.md) verwendet, um zu verschlüsselnde Datenblöcke zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





