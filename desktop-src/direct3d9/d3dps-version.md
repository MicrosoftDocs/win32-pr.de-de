---
description: Erstellen Sie ein Token für die Pixels shader-Version.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION-Makro (D3d9types.h)
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
ms.openlocfilehash: a3958cfaa3afe06e22015a28e8e1ebfd8799c01e89772eb9794dd1249cc0df9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750900"
---
# <a name="d3dps_version-macro"></a>D3DPS \_ VERSION-Makro

Erstellen Sie ein Token für die Pixels shader-Version.

## <a name="syntax"></a>Syntax


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Hauptversion* 
</dt> <dd>

Die Hauptversion des Pixel-Shaders.

</dd> <dt>

*\_Nebenversion* 
</dt> <dd>

Die Version des Nebenpixel-Shaders.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen DWORD-Wert zurück, bei dem es sich um eine Pixel-Shaderversion handelt.

## <a name="remarks"></a>Hinweise

Versionsnummern

Die Versionsnummer ist eine Kombination aus den Versionsnummern der Hauptversion und der Nebenversion des Vertex-Shaders. Gültige Zahlen werden in der Tabelle angezeigt.



| Hauptversion | Nebenversion | Beispiel             |
|-------|-------|---------------------|
| 1     | 1     | D3DPS \_ VERSION(1,1) |
| 1     | 2     | D3DPS \_ VERSION(1,2) |
| 1     | 3     | D3DPS \_ VERSION(1,3) |
| 1     | 4     | D3DPS \_ VERSION(1,4) |
| 2     | 0     | D3DPS \_ VERSION(2,0) |
| 3     | 0     | D3DPS \_ VERSION(3,0) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




