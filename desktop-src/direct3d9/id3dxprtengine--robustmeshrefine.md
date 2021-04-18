---
description: Unterteilt Gesichter in einem Mesh und ermöglicht eine konservative Adaptive Stichprobenentnahme, bei der keine Features im Mesh entfernt werden.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine:: RobustMeshRefine-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365337"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>ID3DXPRTEngine:: RobustMeshRefine-Methode

Unterteilt Gesichter in einem Mesh und ermöglicht eine konservative Adaptive Stichprobenentnahme, bei der keine Features im Mesh entfernt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Minedgelength* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird. Wenn 0 (null), wird ein angemessener Standardwert ersetzt.

</dd> <dt>

*Maxsubdiv* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird. Wenn der Wert 0 (null) ist, wird der Standardwert 5 ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computebounceadaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine:: computedirectlightingshadaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
