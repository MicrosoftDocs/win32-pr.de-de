---
description: Berechnet Einheiten normale für jeden Scheitelpunkt in einem Mesh. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie D3DXComputeTangentFrameEx, um bessere Ergebnisse zu erzielen.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: D3DXComputeNormals-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961654"
---
# <a name="d3dxcomputenormals-function"></a>D3DXComputeNormals-Funktion

Berechnet Einheiten normale für jeden Scheitelpunkt in einem Mesh. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) , um bessere Ergebnisse zu erzielen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das normalisierte Mesh-Objekt darstellt.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im erstellten progressiven Mesh angibt. Dieser Parameter ist optional und sollte auf **null** festgelegt werden, wenn er nicht verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Für das eingabemesh muss das Flag [D3DFVF \_ Normal](d3dfvf.md) in seinem flexiblen Scheitelpunkt Format (FVF) angegeben werden.

Ein normaler Wert für einen Scheitelpunkt wird generiert, indem die normale aller Gesichter, die den Scheitelpunkt teilen, überdurchschnittlich werden.

Wenn eine Angabe bereitgestellt wird, werden replizierte Scheitel Punkte ignoriert und "gegläoniert". Wenn keine Angabe bereitgestellt wird, weisen replizierte Scheitel Punkte, die von nur den Gesichtern abgeleitet werden, die explizit auf Sie verweisen.

Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
