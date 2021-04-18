---
description: Identifiziert Ressourcen Daten. Veraltet.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: Dxfileloadresource-Struktur (dxfile. h)
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
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354390"
---
# <a name="dxfileloadresource-structure"></a>Dxfileloadresource-Struktur

Identifiziert Ressourcen Daten. Veraltet.

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

**HMODULE**
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle des Moduls, das die zu ladende Ressource enthält. Wenn dieser Member **null** ist, muss die Ressource an die ausführbare Datei angefügt werden, von der Sie verwendet wird.

</dd> <dt>

**lpname**
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der zu ladenden Ressource angibt. Wenn die Ressource z. b. ein Mesh ist, sollte dieser Member den Namen der Mesh-Datei angeben.

</dd> <dt>

**lptype**
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Zeiger auf eine Zeichenfolge, die den benutzerdefinierten Typ angibt, der die Ressource identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](idirectxfile--createenumobject.md) " verwendet und dxfileload \_ FromResource angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxfile. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Dateistrukturen](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**"Kreateendumuject"**](idirectxfile--createenumobject.md)
</dt> <dt>

[Dxfile-Konstanten](dxfile.md)
</dt> </dl>

 

 
