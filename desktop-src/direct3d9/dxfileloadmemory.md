---
description: Identifiziert Arbeitsspeicher Daten. Veraltet.
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: Dxfileloadmemory-Struktur (dxfile. h)
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
ms.openlocfilehash: 02424abd354811a6522b58dd0011ecdddce24564
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355032"
---
# <a name="dxfileloadmemory-structure"></a>Dxfileloadmemory-Struktur

Identifiziert Arbeitsspeicher Daten. Veraltet.

## <a name="syntax"></a>Syntax


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>Member

<dl> <dt>

**lpmemory**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf einen Speicherblock, der geladen werden soll.

</dd> <dt>

**dsize**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des zu ladenden Speicherblocks in Bytes.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur identifiziert eine Ressource, die geladen werden soll, wenn eine Anwendung die Methode " [**kreateenumubject**](idirectxfile--createenumobject.md) " verwendet und dxfileload \_ frommemory angibt.

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

 

 
