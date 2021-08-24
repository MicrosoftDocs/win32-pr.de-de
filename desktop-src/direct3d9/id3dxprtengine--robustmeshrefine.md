---
description: Unterteilt Gesichter in ein Gitternetz, sodass eine konservative adaptive Stichprobenentnahme ermöglicht wird, bei der keine Merkmale im Gitternetz entfernt werden.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: ID3DXPRTEngine::RobustMeshRefine-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 280e4552af6de13995ed81afab4d743232485e92446c72b61fd10ae17fea7b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790560"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>ID3DXPRTEngine::RobustMeshRefine-Methode

Unterteilt Gesichter in ein Gitternetz, sodass eine konservative adaptive Stichprobenentnahme ermöglicht wird, bei der keine Merkmale im Gitternetz entfernt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MinEdgeLength* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimale Länge des Gesichtsrands, die bei adaptiver Stichprobenentnahme generiert wird. Bei 0 (null) wird ein angemessener Standardwert ersetzt.

</dd> <dt>

*MaxSubdiv* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Maximale Unterteilung eines Gesichts, das bei der adaptiven Stichprobenentnahme verwendet wird. Wenn 0 (null) ist, wird der Standardwert 5 ersetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
