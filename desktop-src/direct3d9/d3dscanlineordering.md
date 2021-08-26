---
description: Flags, die die Methode angeben, die der Rasterizer verwendet, um ein Bild auf einer Oberfläche zu erstellen.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: D3DSCANLINEORDERING-Enumeration (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987230"
---
# <a name="d3dscanlineordering-enumeration"></a>D3DSCANLINEORDERING-Enumeration

Flags, die die Methode angeben, die der Rasterizer verwendet, um ein Bild auf einer Oberfläche zu erstellen.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ PROGRESSIVE**
</dt> <dd>

Das Image wird von der ersten Scanlinie bis zur letzten erstellt, ohne dass übersprungen wird.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ INTERLACED**
</dt> <dd>

Das Bild wird mithilfe der Interlaced-Methode erstellt, bei der ungerade Zeilen auf ungeraden Durchläufen und gerade Linien auf geraden Läufen gezeichnet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration wird als Member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) und [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




