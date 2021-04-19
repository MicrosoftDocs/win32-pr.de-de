---
description: Berechnen Sie die pro-Dreieck-IMT aus aus den einzelnen Scheitel Punkten. Diese Funktion ermöglicht es Ihnen, das IMT basierend auf einem beliebigen Wert in einem Mesh (Farbe, normal usw.) zu berechnen.
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: D3DXComputeIMTFromPerVertexSignal-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363981"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal-Funktion

Berechnen Sie die pro-Dreieck-IMT aus aus den einzelnen Scheitel Punkten. Diese Funktion ermöglicht es Ihnen, das IMT basierend auf einem beliebigen Wert in einem Mesh (Farbe, normal usw.) zu berechnen.

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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.

</dd> <dt>

*pfvertexsignal* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von pro-Vertex-Daten, aus denen IMT berechnet wird. Die Array Größe ist "usignalstride \* v", wobei "v" die Anzahl der Scheitel Punkte im Mesh ist.

</dd> <dt>

*usignaldimension* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl von Gleit Komma Zahlen pro Scheitelpunkt.

</dd> <dt>

*usignalstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Bytes pro Scheitelpunkt im Array. Dabei muss es sich um ein Vielfaches von sizeof (float) handeln.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Textur Umbruch Optionen. Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).

</dd> <dt>

*pstatus Callback* 
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion zum Überwachen des Fortschritts der IMT-Berechnung.

</dd> <dt>

*pusercontext* 
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine benutzerdefinierte Variable, die an die Status Rückruffunktion übermittelt wird. Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> <dt>

*ppimtdata* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer**](id3dxbuffer.md)), der das zurückgegebene IMT-Array enthält. Dieses Array kann als Eingabe für die D3DX [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Zuordnung des Textur Raums in der Textur Parametrisierung zu priorisieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Verwenden von uvatlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
