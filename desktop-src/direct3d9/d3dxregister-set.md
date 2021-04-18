---
description: Der Datentyp des Registers.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: D3DXREGISTER_SET-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361194"
---
# <a name="d3dxregister_set-enumeration"></a>D3DXREGISTER \_ Set-Enumeration

Der Datentyp des Registers.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ bool**
</dt> <dd>

Boolescher Wert.

</dd> <dt>

<span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**
</dt> <dd>

4D-Ganzzahl.

</dd> <dt>

<span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ float4**
</dt> <dd>

4D-Gleit Komma Zahl.

</dd> <dt>

<span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS- \_ Sampler**
</dt> <dd>

Das Register enthält 4D-Samplingdaten.

</dd> <dt>

<span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ constantinfo**](d3dxshader-constantinfo.md)
</dt> <dt>

[**D3DXCONSTANT- \_ Abteilung**](d3dxconstant-desc.md)
</dt> </dl>

 

 




