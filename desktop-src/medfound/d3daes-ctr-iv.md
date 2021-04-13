---
description: Enthält einen Initialisierungs Vektor (IV) für 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR) Blockchiffre Verschlüsselung.
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342539"
---
# <a name="d3daes_ctr_iv-structure"></a>D3DAES \_ CTR- \_ IV-Struktur

Enthält einen Initialisierungs Vektor (IV) für 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR) Blockchiffre Verschlüsselung.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Member

<dl> <dt>

**IV**
</dt> <dd>

Der IV im Big-Endian-Format.

</dd> <dt>

**Count**
</dt> <dd>

Die Block Anzahl im Big-Endian-Format.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **D3DAES \_ CTR \_ IV** -Struktur und die [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) -Struktur sind gleichwertig.

Weitere Informationen finden Sie unter [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

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

 

 




