---
description: Definiert Transformations Werte für Texturkoordinaten.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: D3DTEXTURETRANSFORMFLAGS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219455"
---
# <a name="d3dtexturetransformflags-enumeration"></a>D3DTEXTURETRANSFORMFLAGS-Enumeration

Definiert Transformations Werte für Texturkoordinaten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ Deaktivieren**
</dt> <dd>

Texturkoordinaten werden direkt an den Rasterizer übermittelt.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

Der Raster sollte 1D-Texturkoordinaten erwarten. Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

Der Raster sollte 2D-Texturkoordinaten erwarten. Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

Der Raster sollte 3D-Texturkoordinaten erwarten. Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

Der Raster sollte 4D-Texturkoordinaten erwarten. Dieser Wert wird von der Vertex-Verarbeitung fester Funktionen verwendet. Er sollte auf 0 festgelegt werden, wenn ein programmierbarer Vertex-Shader verwendet wird.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ projiziert**
</dt> <dd>

Dieses Flag wird durch die Pixel Pipeline der Fixed-Funktion und die programmierbare Pixel Pipeline in den Versionen PS \_ 1 \_ 1 bis PS \_ 1 \_ 3 berücksichtigt. Wenn die Textur Projektion für eine Textur Phase aktiviert ist, müssen alle vier Gleit Komma Werte in das entsprechende Textur Register geschrieben werden. Jede Textur Koordinate wird durch das letzte Element dividiert, bevor Sie an den Rasterizer übermittelt wird. Wenn dieses Flag z. b. mit dem D3DTTFF \_ COUNT3-Flag angegeben wird, werden die erste und zweite Textur Koordinate durch die dritte Koordinate dividiert, bevor Sie an den Rasterizer übermittelt werden.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Texturkoordinaten können mithilfe einer 4 x 4-Matrix transformiert werden, bevor die Ergebnisse an den Rasterizer übermittelt werden. Die Texturkoordinaten Transformationen werden durch Aufrufen von [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api)und durch Übergeben des D3DTSS \_ texturetransformflags-Textur Phasen Zustands und eines der Werte aus **D3DTEXTURETRANSFORMFLAGS** festgelegt. Weitere Informationen zu Textur Transformationen finden Sie unter [Texturkoordinaten Transformationen (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
