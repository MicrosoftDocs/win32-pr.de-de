---
description: Enthält einen Initialisierungsvektor (IV) für die Blockchiffreverschlüsselung im 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV-Struktur (D3d9types.h)
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
ms.openlocfilehash: 09535b432ff1af60ad33b622810d0d8a4d190cb81650214aa71b445ba3c22f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974789"
---
# <a name="d3daes_ctr_iv-structure"></a>D3DAES \_ CTR \_ IV-Struktur

Enthält einen Initialisierungsvektor (IV) für die Blockchiffreverschlüsselung im 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR).

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

Die Blockanzahl im Big-Endian-Format.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **D3DAES \_ CTR \_ IV-Struktur** und die [**DXVA2 \_ AES \_ CTR \_ IV-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sind gleichwertig.

Weitere Informationen finden Sie unter [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (einschließlich D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> </dl>

 

 




