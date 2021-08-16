---
description: Identifiziert Ressourcendaten. Veraltet.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: DXFILELOADRESOURCE-Struktur (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803037"
---
# <a name="dxfileloadresource-structure"></a>DXFILELOADRESOURCE-Struktur

Identifiziert Ressourcendaten. Veraltet.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>Member

<dl> <dt>

**hModule**
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle des Moduls, das die zu ladende Ressource enthält. Wenn dieser Member **NULL** ist, muss die Ressource an die ausführbare Datei angefügt werden, die sie verwenden wird.

</dd> <dt>

**lpName**
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt. Wenn die Ressource beispielsweise ein Gitternetz ist, sollte dieser Member den Namen der Gitternetzdatei angeben.

</dd> <dt>

**lpType**
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die [**CreateEnumObject-Methode**](idirectxfile--createenumobject.md) verwendet, und gibt DXFILELOAD \_ FROMRESOURCE an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXFile.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[X-Dateistrukturen](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[DXFILE-Konstanten](dxfile.md)
</dt> </dl>

 

 
