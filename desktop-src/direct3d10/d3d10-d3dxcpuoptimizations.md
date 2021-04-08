---
description: Aktiviert oder deaktiviert CPU-Optimierungen.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: D3DXCpuOptimizations-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762201"
---
# <a name="d3dxcpuoptimizations-function"></a>D3DXCpuOptimizations-Funktion

Aktiviert oder deaktiviert CPU-Optimierungen.

## <a name="syntax"></a>Syntax


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktivieren* \[ von in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

" **True** ", um CPU-Optimierungen zu aktivieren; andernfalls **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: **[ **D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)**

Gibt den Typ der erkannten CPU zurück, für den Optimierungen vorhanden sind (siehe [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
