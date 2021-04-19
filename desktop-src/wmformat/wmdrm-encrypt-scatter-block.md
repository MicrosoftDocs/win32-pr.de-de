---
title: WMDRM_ENCRYPT_SCATTER_BLOCK Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Verschlüsselungs Punkt \_ \_ Blockstruktur enthält einen Daten Block, der verschlüsselt werden soll.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
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
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353821"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>WMDRM-Verschlüsselungs Punkt- \_ \_ \_ Block Struktur

Die **WMDRM- \_ Verschlüsselungs Punkt \_ \_ Block** Struktur enthält einen Daten Block, der verschlüsselt werden soll.

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

**dwstreamid**
</dt> <dd>

Der Bezeichner des Streams, zu dem der Datenblock gehört.

</dd> <dt>

**cbblock**
</dt> <dd>

Blockgröße in Bytes.

</dd> <dt>

**pbblock**
</dt> <dd>

Zeiger auf einen Puffer, der den Datenblock enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von der [**iwmdrmencryptscatter:: verschlüsseltscatter**](iwmdrmencryptscatter-encryptscatter.md) -Methode verwendet, um Datenblöcke zu identifizieren, die verschlüsselt werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





