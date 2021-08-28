---
description: Berechnen sie Tangens,binormale und normale Vektoren für ein Gitter.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: D3DXComputeTangentFrame-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 532b265f387179d88581f6f0a05227162de6a8402e324e7be2e13a16ca4a3ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849830"
---
# <a name="d3dxcomputetangentframe-function"></a>D3DXComputeTangentFrame-Funktion

Berechnen sie Tangens,binormale und normale Vektoren für ein Gitter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***

Zeiger auf ein [**Eingabe-ID3DXMesh-Gittermodellobjekt.**](id3dxmesh.md)

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus mindestens einem [**D3DXTANGENT-Flag.**](./d3dxtangent.md)

Verwenden **Sie NULL,** um die folgenden Optionen anzugeben:

-   Gewichten Sie die normale Vektorlänge nach dem Winkel im Bogenmaß, der von den beiden Kanten, die den Scheitelpunkt verlassen, unterstützt wird.
-   Berechnen Sie orthogonale kartesische Koordinaten aus den UV-Texturkoordinaten.
-   Texturen sind nicht in U- oder V-Richtungen umschlossen.
-   Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.
-   Scheitelpunkts werden gegen den Uhrzeigersinn um jedes Dreieck herum geordnet.
-   Verwenden Sie normale Vektoren pro Scheitelpunkt, die bereits im Eingabegitternetz vorhanden sind.
-   Die Ergebnisse werden im ursprünglichen Eingabegitter gespeichert. Die Funktion erzeugt einen Fehler, wenn neue Scheitelungen erstellt werden müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion ruft einfach [**D3DXComputeTangentFrameEx mit**](d3dxcomputetangentframeex.md) den folgenden Eingabeparametern auf:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Singularitäten werden nach Bedarf durch Gruppieren von Kanten und Teilen von Scheitelpunkt behandelt. Wenn Scheitelungen aufgeteilt werden müssen, kann die Funktion nicht verwendet werden. Der berechnete Normalvektor an jedem Scheitelpunkt wird immer normalisiert, um eine Einheitenlänge zu haben.

Die stabilste Lösung zum Berechnen von orthogonalen kartesischen Koordinaten besteht in der Nicht-Kennzeichnung von D3DXTANGENT \_ ORTHOGONALIZE FROM you und \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, sodass \_ \_ orthogonale Koordinaten aus beiden UV-Texturkoordinaten berechnet werden. Wenn jedoch in diesem Fall U oder V null ist, berechnet die Funktion orthogonale Koordinaten mithilfe von D3DXTANGENT ORTHOGONALIZE FROM V bzw. \_ \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
