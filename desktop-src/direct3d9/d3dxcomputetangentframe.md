---
description: Compute Tangens, Binormale und normale Vektoren für ein Mesh.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: D3DXComputeTangentFrame-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353761"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame-Funktion

Compute Tangens, Binormale und normale Vektoren für ein Mesh.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von mindestens einem [**D3DXTANGENT**](./d3dxtangent.md) -Flags.

Verwenden Sie **null** , um die folgenden Optionen anzugeben:

-   Gewichtung der normalen Vektor Länge um den Winkel im Bogenmaße, der von den beiden Kanten, die den Scheitelpunkt hinterlassen, untergeordneter Länge liegt.
-   Berechnen Sie orthogonale kartesische Koordinaten aus den UV-Texturkoordinaten.
-   Texturen sind weder in der U-noch in der V-Richtung umschließt
-   Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.
-   Vertices werden um jedes Dreieck in der Richtung gegen den Uhrzeigersinn angeordnet.
-   Verwenden Sie die pro-Vertex-normal Vektoren, die bereits im Eingabe Mesh vorhanden sind.
-   Die Ergebnisse werden im ursprünglichen Eingabe Mesh gespeichert. Die Funktion schlägt fehl, wenn neue Vertices erstellt werden müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) mit den folgenden Eingabe Parametern auf:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt. Wenn Vertices aufgeteilt werden müssen, schlägt die Funktion fehl. Der berechnete normale Vektor bei jedem Scheitelpunkt wird immer normalisiert, sodass er über eine Einheitslänge verfügt.

Die stabilste Lösung für die Berechnung von orthogonalen kartesischen Koordinaten ist das Festlegen von Flags D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ V, sodass orthogonale Koordinaten aus beiden UV-Texturkoordinaten berechnet werden. Wenn in diesem Fall jedoch entweder "U" oder "V" gleich NULL ist, berechnet die Funktion orthogonale Koordinaten mithilfe von D3DXTANGENT \_ orthogonalize \_ von \_ V bzw \_ . D3DXTANGENT orthogonalize \_ von \_ U bzw..

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
