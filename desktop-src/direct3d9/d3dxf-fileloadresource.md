---
description: Identifiziert Ressourcendaten.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: D3DXF_FILELOADRESOURCE -Struktur (D3dx9xof.h)
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
ms.openlocfilehash: ddc105d3df7732e1572e41c3d9cb47a285caf69cba0a24f6ea65090706394592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564930"
---
# <a name="d3dxf_fileloadresource-structure"></a>D3DXF \_ FILELOADRESOURCE-Struktur

Identifiziert Ressourcendaten.

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

**hModule**
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle des Moduls, das die zu ladende Ressource enthält. Wenn dieser Member **NULL ist,** muss die Ressource an die ausführbare Datei angefügt werden, die sie verwendet.

</dd> <dt>

**lpName**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt. Wenn die Ressource beispielsweise ein Gitternetz ist, sollte dieser Member den Namen der Meshdatei angeben.

</dd> <dt>

**lpType**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur identifiziert eine zu ladende Ressource, wenn eine Anwendung die [**CreateEnumObject-Methode**](id3dxfile--createenumobject.md) verwendet, und gibt das [Flag D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateistrukturen](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
