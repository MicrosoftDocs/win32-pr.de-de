---
description: Beschreibt eine Oberfläche.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b18c9cd3428463f82a6e243a57ade3fffd650bb35f2c73234b725fa5bf0607eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300232"
---
# <a name="d3dsurface_desc-structure"></a>D3DSURFACE \_ DESC-Struktur

Beschreibt eine Oberfläche.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Oberflächenformat beschreibt.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE-Enumerationstyps,**](./d3dresourcetype.md) der diese Ressource als Oberfläche identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Entweder die D3DUSAGE \_ DEPTHSTENCIL- oder D3DUSAGE \_ RENDERTARGET-Werte. Weitere Informationen finden Sie unter [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Für diese Oberfläche zugeordnete Speicherklasse angibt.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Typ: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Member des [**D3DMULTISAMPLE TYPE-Enumerationstyps, \_**](./d3dmultisample-type.md) der die Ebenen der von der Oberfläche unterstützten Vollszenen-Multisampling angibt.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualitätsstufe. Der gültige Bereich liegt zwischen 0 (null) und 1 kleiner als die von "pQualityLevels" zurückgegebene Ebene, die von [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)verwendet wird. Wenn Sie einen größeren Wert übergeben, wird der Fehler D3DERR \_ INVALIDCALL zurückgegeben. Die MultisampleQuality-Werte von gekoppelten Renderzielen, Tiefenschablonenoberflächen und dem MultiSample-Typ müssen übereinstimmen.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Oberfläche in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Oberfläche in Pixel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
