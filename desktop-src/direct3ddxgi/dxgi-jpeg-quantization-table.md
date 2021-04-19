---
description: Beschreibt eine JPEG-quantisierungstabelle.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: DXGI_JPEG_QUANTIZATION_TABLE-Struktur (dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361858"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a>DXGI- \_ JPEG- \_ quantisierungstabellenstruktur \_

Beschreibt eine JPEG-quantisierungstabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**Elemente**
</dt> <dd>

Ein Bytearray, das die Elemente der quantifizierungstabelle enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Strukturen](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




