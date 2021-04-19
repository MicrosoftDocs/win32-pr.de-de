---
description: Identifiziert Ressourcen Daten.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE-Struktur (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366465"
---
# <a name="d3dxf_fileloadresource-structure"></a>D3DXF \_ fileloadresource-Struktur

Identifiziert Ressourcen Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a>Member

<dl> <dt>

**HMODULE**
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle des Moduls, das die zu ladende Ressource enthält. Wenn dieser Member **null** ist, muss die Ressource an die ausführbare Datei angefügt werden, von der Sie verwendet wird.

</dd> <dt>

**lpname**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt. Wenn die Ressource z. b. ein Mesh ist, sollte dieser Member den Namen der Mesh-Datei angeben.

</dd> <dt>

**lptype**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](id3dxfile--createenumobject.md) " verwendet und das Flag " [D3DXF \_ fileload \_ FromResource](d3dxf.md) " angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateistrukturen](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
