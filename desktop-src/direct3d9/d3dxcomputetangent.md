---
description: Berechnet die Tangenten Vektoren für die in der Textur Phase angegebenen Texturkoordinaten. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie D3DXComputeTangentFrameEx, um bessere Ergebnisse zu erzielen.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: D3DXComputeTangent-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366638"
---
# <a name="d3dxcomputetangent-function"></a>D3DXComputeTangent-Funktion

Berechnet die Tangenten Vektoren für die in der Textur Phase angegebenen Texturkoordinaten. Wird zur Unterstützung von Legacy Anwendungen bereitgestellt. Verwenden Sie [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) , um bessere Ergebnisse zu erzielen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das Eingabe Mesh darstellt.

</dd> <dt>

*Texstagumdex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Index, der die Textur Phase darstellt.

</dd> <dt>

*Tangentindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index, der den Verwendungs Index für die Tangens Daten bereitstellt. Die Vertex-Deklaration impliziert die Verwendung. Dieser Index ändert die Verwendung mit dem Verwendungs Index. Weitere Informationen zu einer Scheitelpunkt Deklaration finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Binormindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Index, der den Verwendungs Index für die Binärdaten bereitstellt. Die Vertex-Deklaration impliziert die Verwendung. Dieser Index ändert die Verwendung mit dem Verwendungs Index. Weitere Informationen zu einer Scheitelpunkt Deklaration finden Sie unter [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

 Umbruch \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Legen Sie diesen Wert auf 0 (null) fest, um keine Umbrüchen zu erhalten.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit angrenzenden Gesichts Indizes aufgefüllt werden soll. Die Anzahl der Bytes in diesem Array muss mindestens ((3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)) betragen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Wenn die Mesh-Vertex-Deklaration Tangens-oder Binormale-Felder angibt, aktualisiert **D3DXComputeTangent** alle vom Benutzer bereitgestellten Tangens-oder Binärdaten. Alternativ können Sie tangentindex auf [D3DX \_ default](other-d3dx-constants.md) festlegen, um die vom Benutzer bereitgestellten Tangens Daten nicht zu aktualisieren, oder binormindex auf D3DX default festlegen, \_ um die vom Benutzer bereitgestellten Binärdaten nicht zu aktualisieren. Texstageindex kann nicht auf D3DX Default festgelegt werden \_ .

**D3DXComputeTangent** hängt von der Mesh-Vertexdeklaration ab, die entweder das Binormal-Feld (binormindex), das Tangens Feld (tangentindex) oder beides enthält. Wenn beide fehlen, schlägt diese Funktion fehl.

Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
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

 

 
