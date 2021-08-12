---
description: Berechnet imT-Werte pro Dreieck aus einem benutzerdefinierten anwendungsspezifischen Signal, das über die Oberfläche des Gitters variiert (im Allgemeinen mit einer höheren Frequenz als Scheitelpunktdaten). Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: D3DXComputeIMTFromSignal-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 9d645e12f7159963f9b9bc5abeb960aee0bac2282537c482465be3ea08690181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299412"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>D3DXComputeIMTFromSignal-Funktion

Berechnet imT-Werte pro Dreieck aus einem benutzerdefinierten anwendungsspezifischen Signal, das über die Oberfläche des Gitters variiert (im Allgemeinen mit einer höheren Frequenz als Scheitelpunktdaten). Das Signal wird über eine vom Benutzer angegebene Rückruffunktion ausgewertet.

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

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des IMT enthält.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der an identifiziert, welche Texturkoordinaten verwendet werden.

</dd> <dt>

*uSignalDimension* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Komponenten in jedem Datenpunkt im Signal.

</dd> <dt>

*fMaxUVDistance* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der maximale Abstand zwischen Scheiteltices; Der Algorithmus setzt die Unterteilung fort, bis der Abstand zwischen allen Scheitelpunkt kleiner oder gleich fMaxUVDistance ist.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Texturumbruchoptionen. Dies ist eine Kombination aus mindestens einem [**D3DXIMT-FLAGS.**](./d3dximt-flags.md)

</dd> <dt>

*pSignalCallback* \[ In\]
</dt> <dd>

Typ: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Ein Zeiger auf eine vom Benutzer bereitgestellte Auswertungsfunktion, die verwendet wird, um den Signalwert an beliebigen U,V-Koordinaten zu berechnen. Die Funktion folgt dem Prototyp von [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*pUserData* \[ In\]
</dt> <dd>

Typ: **\* VOID**

Ein Zeiger auf einen benutzerdefinierten Wert, der an die Signalrückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.

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

## <a name="remarks"></a>Hinweise

Diese Funktion erfordert, dass das Eingabegitter eine Signal-zu-Mesh-Texturzuordnung (d. h. Texturkoordinaten) enthält. Es ermöglicht dem Benutzer, ein Signal willkürlich über der Oberfläche des Gitters zu definieren.

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

 

 
