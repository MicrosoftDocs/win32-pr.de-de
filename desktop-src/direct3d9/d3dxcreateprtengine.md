---
description: Erstellt ein ID3DXPRTEngine-Objekt, das die PRT-Simulationen (preberechnete Strahlen Übertragung) einer 3D-Szene effizient generieren kann.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: D3DXCreatePRTEngine-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530929"
---
# <a name="d3dxcreateprtengine-function"></a>D3DXCreatePRTEngine-Funktion

Erstellt ein [**ID3DXPRTEngine**](id3dxprtengine.md) -Objekt, das die PRT-Simulationen (preberechnete Strahlen Übertragung) einer 3D-Szene effizient generieren kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt, das die 3D-Szene modelliert. Dieses Mesh muss über eine Attribut Tabelle verfügen, in der Vertices in einem eindeutigen Attribut enthalten sind.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Optionaler Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit angrenzenden Gesichts Indizes aufgefüllt werden soll. Die Anzahl der Bytes in diesem Array muss mindestens ((3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)) betragen. Kann **null** sein.

</dd> <dt>

*Extractuvs* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass Texturen zum Speichern von Albedos-oder PRT-Vektoren verwendet werden.

</dd> <dt>

*pblockermesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein optionales [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, das die 3D-Szene blockiert. Kann **null** sein.

</dd> <dt>

*ppengine* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Zeiger auf ein Output [**ID3DXPRTEngine**](id3dxprtengine.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) , um mehrere Netzen zu einer einzelnen Gitter Schnittstelle zu kombinieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
