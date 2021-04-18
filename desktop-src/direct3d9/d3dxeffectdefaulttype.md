---
description: Effekt Datentypen. Die Daten sind im pValue-Member von D3DXEFFECTDEFAULT enthalten.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: D3DXEFFECTDEFAULTTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354371"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a>D3DXEFFECTDEFAULTTYPE-Enumeration

Effekt Datentypen. Die Daten sind im pValue-Member von [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)enthalten.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT- \_ Zeichenfolge**
</dt> <dd>

Der-Datentyp ist eine NULL-terminierte ASCII-Text Zeichenfolge.

</dd> <dt>

<span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ float**
</dt> <dd>

Der Datentyp ist ein Array vom Typ "float". Die Anzahl von float-Typen im Array wird durch numBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)angegeben.

</dd> <dt>

<span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT- \_ DWORD**
</dt> <dd>

Der Datentyp ist ein DWORD.

</dd> <dt>

<span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ forcedword**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




