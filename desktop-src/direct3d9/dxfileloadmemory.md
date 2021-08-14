---
description: Identifiziert Speicherdaten. Veraltet.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: DXFILELOADMEMORY-Struktur (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 3de6db80e12197f3ad61dd845519be7f532d320765c491cba7a8219ee701af05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407460"
---
# <a name="dxfileloadmemory-structure"></a>DXFILELOADMEMORY-Struktur

Identifiziert Speicherdaten. Veraltet.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Member

<dl> <dt>

**lpMemory**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf einen Speicherblock, der geladen werden soll.

</dd> <dt>

**dSize**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des zu ladenden Speicherblocks in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur identifiziert eine Zu ladende Ressource, wenn eine Anwendung die [**CreateEnumObject-Methode**](idirectxfile--createenumobject.md) verwendet, und gibt DXFILELOAD \_ FROMMEMORY an.

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

 

 
