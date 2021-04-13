---
description: Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine:: setminmaxschnitt-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355147"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>ID3DXPRTEngine:: setminmaxschnitt-Methode

Legt den minimalen und maximalen Abstand der Schnittmenge zwischen 3D-Objekten fest. Diese Entfernungs Werte können verwendet werden, um die minimale oder maximale Entfernung zu steuern, die Objekte durch Schatten oder Licht widerspiegeln können. Beispielsweise kann die-Methode verwendet werden, um den shadodown der in der Nähe befindlichen Funktionen eines 3D-Modells einzuschränken.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

der- *Administrator* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimale Überschneidungs Abweichung. Muss positiv und kleiner als der Wert von "f" sein.

</dd> <dt>

mit dem Namen  \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximale Schnittstellen Länge. Wenn 0,0 f, wird der vorherige Wert verwendet. Andernfalls muss größer als der Wert von "f" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht in PRT-Simulationen (preberechneten Radiance Transfer) verwendet werden, die in der GPU ausgeführt werden. Weitere Informationen finden Sie unter [**ID3DXPRTEngine:: computedirectlightingshgpu**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
