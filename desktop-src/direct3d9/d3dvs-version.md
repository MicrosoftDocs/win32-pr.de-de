---
description: Erstellen Sie ein Vertex-Shader-Versionsnummern Token.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373528"
---
# <a name="d3dvs_version-macro"></a>D3DVS- \_ Versions Makro

Erstellen Sie ein Vertex-Shader-Versionsnummern Token.

## <a name="syntax"></a>Syntax


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Wichtige* 
</dt> <dd>

Die Hauptversion des Vertex-Shaders. Entsprechende Werte finden Sie unter "Hinweise".

</dd> <dt>

*\_Nebenversion* 
</dt> <dd>

Die kleinere Scheitelpunkt-Shader-Version. Entsprechende Werte finden Sie unter "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen DWORD-Wert zurück, der eine Scheitelpunkt-Shader-Version ist.

## <a name="remarks"></a>Bemerkungen

Versionsnummern

Die Versionsnummer ist eine Kombination aus der Hauptversion und den kleineren Scheitelpunkt-Shader-Versionsnummern. In der Tabelle werden gültige Zahlen angezeigt.



| Hauptversion | Nebenversion | Beispiel             |
|-------|-------|---------------------|
| 1     | 1     | D3DVS- \_ Version (1, 1) |
| 2     | 0     | D3DVS- \_ Version (2, 0) |
| 3     | 0     | D3DVS- \_ Version (3, 0) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




