---
description: Definiert Konstanten, die die unterstützten Textur Adressierungs Modi beschreiben.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: D3DTEXTUREADDRESS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050842"
---
# <a name="d3dtextureaddress-enumeration"></a>D3DTEXTUREADDRESS-Enumeration

Definiert Konstanten, die die unterstützten Textur Adressierungs Modi beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Wrap**
</dt> <dd>

Kacheln Sie die Textur bei jeder ganzzahligen Verknüpfung. Wenn Sie z. b. Werte zwischen 0 und 3 haben, wird die Textur dreimal wiederholt. Es wird keine Spiegelung durchgeführt.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS- \_ Spiegelung**
</dt> <dd>

Vergleichbar mit D3DTADDRESS \_ Wrap, mit der Ausnahme, dass die Textur bei jeder ganzzahligen Verknüpfung gekippt wird. bei Werten zwischen 0 und 1 wird die Textur z. b. normal behandelt. zwischen 1 und 2 wird die Textur gekippt (gespiegelt). zwischen 2 und 3 ist die Textur wieder normal. Und so weiter.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS- \_ Klammer**
</dt> <dd>

Texturkoordinaten außerhalb des Bereichs \[ 0,0, 1,0 \] werden auf die Textur Farbe bei 0,0 oder 1,0 festgelegt.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS \_ -Rahmen**
</dt> <dd>

Texturkoordinaten außerhalb des Bereichs \[ 0,0, 1,0 \] werden auf die Rahmenfarbe festgelegt.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ mirroronce**
</dt> <dd>

Vergleichbar mit D3DTADDRESS \_ Mirror und D3DTADDRESS \_ Clamp. Nimmt den absoluten Wert der Textur Koordinate (also die Spiegelung um 0) und bindet dann an den maximalen Wert. Die häufigste Verwendung ist für volumetexturen, bei denen die Unterstützung für den vollständigen D3DTADDRESS \_ mirroronce-Textur Adressierungs Modus nicht erforderlich ist, aber die Daten um die eine Achse symmetrisch sind.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
