---
description: Berechnen Sie imT-Werte pro Dreieck aus Daten pro Scheitelpunkt. Mit dieser Funktion können Sie den IMT basierend auf einem beliebigen Wert in einem Gitternetz (Farbe, Normal usw.) berechnen.
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: D3DXComputeIMTFromPerVertexSignal-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41d635bf436e139e4c44db75b1057cebc3a50cfee114a35bfc75a9de84abc404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299457"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal-Funktion

Berechnen Sie imT-Werte pro Dreieck aus Daten pro Scheitelpunkt. Mit dieser Funktion können Sie den IMT basierend auf einem beliebigen Wert in einem Gitternetz (Farbe, Normal usw.) berechnen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objektgeometrie zum Berechnen des IMT enthält.

</dd> <dt>

*pfVertexSignal* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von Pro-Scheitelpunkt-Daten, aus denen IMT berechnet wird. Die Arraygröße ist uSignalStride v, wobei v die Anzahl \* der Scheitelzeichen im Gitternetz ist.

</dd> <dt>

*uSignalDimension* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Gleitkommazahlen pro Scheitelpunkt.

</dd> <dt>

*uSignalStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Bytes pro Scheitelpunkt im Array. Dies muss ein Vielfaches von sizeof(float) sein.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Texturumbruchoptionen. Dies ist eine Kombination aus mindestens einem [**D3DXIMT-FLAGS.**](./d3dximt-flags.md)

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion zum Überwachen des IMT-Berechnungsfortschritts.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine benutzerdefinierte Variable, die an die Statusrückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer),**](id3dxbuffer.md)der das zurückgegebene IMT-Array enthält. Dieses Array kann als Eingabe für die D3DX [UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Texturraumzuordnung in der Texturparameterisierung zu priorisieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D OK, andernfalls ist der Wert \_ D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Verwenden von UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
