---
description: Vordefinierte Sätze von Pipeline Zuständen, die von Zustands Blöcken verwendet werden (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: D3DSTATEBLOCKTYPE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104551698"
---
# <a name="d3dstateblocktype-enumeration"></a>D3DSTATEBLOCKTYPE-Enumeration

Vordefinierte Sätze von Pipeline Zuständen, die von Zustands Blöcken verwendet werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).

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

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_**
</dt> <dd>

Erfassen des aktuellen [Geräte Zustands](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ Pixel State**
</dt> <dd>

Erfassen des aktuellen [Pixel Zustands](saving-pixel-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ vertexstate**
</dt> <dd>

Erfassen des aktuellen [Scheitelpunkt Zustands](saving-vertex-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Verwenden Sie diesen Wert nicht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wie im folgenden Diagramm gezeigt, sind Scheitelpunkt-und Pixel Status beide Teilmengen des Geräte Zustands.

![Diagramm des Geräte Zustands mit vertexzustand und Pixel Zustand als Teilmengen](images/statesets.png)

Es gibt nur wenige Zustände, die als Scheitelpunkt und Pixel Status betrachtet werden. Folgende Status sind möglich:

-   Rendering-Status: D3DRS \_ fogdensity
-   Rendering-Status: D3DRS \_ fogstart
-   Rendering-Status: D3DRS \_ fogend
-   Textur Zustand: D3DTSS \_ texcoordindex
-   Textur Zustand: D3DTSS \_ texturetransformflags

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: kreatestateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9:: kreatestateblock**
</dt> </dl>

 

 
