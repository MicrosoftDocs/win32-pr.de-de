---
description: Beschreibt eine Oberfläche.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351941"
---
# <a name="d3dsurface_desc-structure"></a>D3DSURFACE- \_ Struktur

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

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format beschreibt.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Oberfläche identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Entweder die D3DUSAGE \_ depthstencil-oder D3DUSAGE \_ renderTarget-Werte. Weitere Informationen finden Sie unter [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für diese Oberfläche zugeordnete Arbeitsspeicher Klasse angibt.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Type: **[ **D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md)**

</dd> <dd>

Member des Typs " [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) enumerieriert", der die Ebenen der von der-Oberfläche unterstützten vollständigen multisamplinggrad-Auflistung angibt.

</dd> <dt>

**Multisamplequality**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualitätsstufe. Der gültige Bereich liegt zwischen 0 (null) und einem niedrigeren Wert als der von " [**checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)" verwendeten pqualitylevels. Wenn Sie einen größeren Wert übergeben, wird der Fehler "D3DERR \_ invalidcall" zurückgegeben. Die multisamplequality-Werte von gekoppelten renderzielen, tiefen Schablone-Oberflächen und der Multisample-Typ müssen alle entsprechen.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Oberfläche in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Oberfläche in Pixel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getleveldebug**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**Getleveldebug**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
