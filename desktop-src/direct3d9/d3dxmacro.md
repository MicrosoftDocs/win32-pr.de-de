---
description: Beschreibt die von einem Effekt Objekt verwendeten Präprozessordefinitionen.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: D3DXMACRO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363995"
---
# <a name="d3dxmacro-structure"></a>D3DXMACRO-Struktur

Beschreibt die von einem Effekt Objekt verwendeten Präprozessordefinitionen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Der präprozessorname.

</dd> <dt>

**Definition**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Definitions Name.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um **D3DXMACRO** s in mehr als einer Zeile zu verwenden, stellen Sie jedem neuen Zeilenzeichen einen umgekehrten Schrägstrich (wie z \# . b. eine Definition in der Programmiersprache C) voran. Beispiel:


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Beachten Sie die drei umgekehrten Schrägstriche am Ende der Zeile. Die ersten beiden sind erforderlich, um ein einzelnes ' \\ ', gefolgt vom Zeilen vorzeilenzeichen " \\ n" auszugeben. Optional können Sie auch Ihre Zeilen mit " \\ \\ \\ r \\ n" beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
