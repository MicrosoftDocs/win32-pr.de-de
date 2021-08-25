---
description: Vordefinierte Pipelinezustandssätze, die von Zustandsblöcken verwendet werden (siehe Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: D3DSTATEBLOCKTYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850185"
---
# <a name="d3dstateblocktype-enumeration"></a>D3DSTATEBLOCKTYPE-Enumeration

Vordefinierte Pipelinezustandssätze, die von Zustandsblöcken verwendet werden (siehe [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ ALL**
</dt> <dd>

Erfassen Sie den aktuellen [Gerätezustand.](saving-all-device-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Erfassen Sie den aktuellen [Pixelzustand.](saving-pixel-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Erfassen Sie den aktuellen [Scheitelpunktzustand.](saving-vertex-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Verwenden Sie diesen Wert nicht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wie das folgende Diagramm zeigt, sind Der Scheitelpunkt und der Pixelzustand beide Teilmengen des Gerätezustands.

![Diagramm des Gerätezustands mit Scheitelpunktzustand und Pixelzustand als Teilmengen](images/statesets.png)

Es gibt nur wenige Zustände, die sowohl als Scheitelpunkt- als auch als Pixelzustand betrachtet werden. Folgende Status sind möglich:

-   Renderzustand: D3DRS- \_ UND -NSSITY
-   Renderzustand: D3DRS \_ VERSCHENKSTART
-   Renderzustand: D3DRS– \_ ADREND
-   Texturzustand: D3DTSS \_ TEXCOORDINDEX
-   Texturzustand: D3DTSS \_ TEXTURETRANSFORMFLAGS

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
