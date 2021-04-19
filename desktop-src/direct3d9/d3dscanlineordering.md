---
description: Flags, die die Methode angeben, die der Raster zum Erstellen eines Bilds auf einer Oberfläche verwendet.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: D3DSCANLINEORDERING-Enumeration (D3d9types. h)
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
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367399"
---
# <a name="d3dscanlineordering-enumeration"></a>D3DSCANLINEORDERING-Enumeration

Flags, die die Methode angeben, die der Raster zum Erstellen eines Bilds auf einer Oberfläche verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressiv**
</dt> <dd>

Das Bild wird von der ersten Scanline bis zum letzten erstellt, ohne dass übersprungen wird.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING-Zeilen Sprung \_**
</dt> <dd>

Das Bild wird mit der Zeilen Sprung Methode erstellt, in der ungerade nummerierte Linien bei ungeraden nummerierten Durchläufen gezeichnet werden und sogar Linien bei geraden Durchläufen gezeichnet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird als Member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) und [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




