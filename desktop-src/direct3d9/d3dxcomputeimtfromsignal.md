---
description: Berechnet pro Dreieck von einem benutzerdefinierten, von der Anwendung angegebenen Signal, das sich über der Oberfläche des Netzes (in der Regel mit einer höheren Frequenz als Scheitelpunkt Daten) unterscheidet. Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: D3DXComputeIMTFromSignal-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363155"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>D3DXComputeIMTFromSignal-Funktion

Berechnet pro Dreieck von einem benutzerdefinierten, von der Anwendung angegebenen Signal, das sich über der Oberfläche des Netzes (in der Regel mit einer höheren Frequenz als Scheitelpunkt Daten) unterscheidet. Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabe Gitter (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des IMTS enthält.

</dd> <dt>

*dwtextureindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*usignaldimension* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Komponenten in jedem Datenpunkt im Signal.

</dd> <dt>

*fmaxuvdistance* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der maximale Abstand zwischen Scheitel Punkten; der Algorithmus setzt die Unterteilung fort, bis der Abstand zwischen allen Scheitel Punkten kleiner oder gleich fmaxuvdistance ist.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Textur Umbruch Optionen. Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-Flags**](./d3dximt-flags.md).

</dd> <dt>

*psignalcallback* \[ in\]
</dt> <dd>

Typ: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Ein Zeiger auf eine vom Benutzer bereitgestellte evaluatorfunktion, die verwendet wird, um den Signalwert bei beliebigen U-, V-Koordinaten zu berechnen. Die-Funktion folgt dem Prototyp von [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*puserdata* \[ in\]
</dt> <dd>

Typ: **void \***

Ein Zeiger auf einen benutzerdefinierten Wert, der an die Signal Rückruffunktion übermittelt wird. Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

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

## <a name="remarks"></a>Bemerkungen

Diese Funktion erfordert, dass das eingabemesh eine Signal-zu-Mesh-Textur Zuordnung (d.h. Texturkoordinaten) enthält. Dadurch kann der Benutzer ein Signal willkürlich über der Oberfläche des Netzes definieren.

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

 

 
