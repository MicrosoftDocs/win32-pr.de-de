---
description: Erstellen Sie ein Pixel-Shader-Versions Token.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355047"
---
# <a name="d3dps_version-macro"></a>D3DPS- \_ Versions Makro

Erstellen Sie ein Pixel-Shader-Versions Token.

## <a name="syntax"></a>Syntax


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Wichtige* 
</dt> <dd>

Die Haupt-Pixel-Shader-Version.

</dd> <dt>

*\_Nebenversion* 
</dt> <dd>

Die neben Version des Pixelshaders.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen DWORD-Wert zurück, der eine Pixel-Shader-Version ist.

## <a name="remarks"></a>Bemerkungen

Versionsnummern

Die Versionsnummer ist eine Kombination aus der Hauptversion und den kleineren Scheitelpunkt-Shader-Versionsnummern. In der Tabelle werden gültige Zahlen angezeigt.



| Hauptversion | Nebenversion | Beispiel             |
|-------|-------|---------------------|
| 1     | 1     | D3DPS- \_ Version (1, 1) |
| 1     | 2     | D3DPS- \_ Version (1, 2) |
| 1     | 3     | D3DPS- \_ Version (1, 3) |
| 1     | 4     | D3DPS- \_ Version (1, 4) |
| 2     | 0     | D3DPS- \_ Version (2, 0) |
| 3     | 0     | D3DPS- \_ Version (3, 0) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




