---
description: Führt Tangens-Frame Berechnungen in einem Mesh aus. Tangens, Binormale und optional normale Vektoren werden generiert. Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: D3DXComputeTangentFrameEx-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365294"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx-Funktion

Führt Tangens-Frame Berechnungen in einem Mesh aus. Tangens, Binormale und optional normale Vektoren werden generiert. Singularitäten werden nach Bedarf durch Gruppierung von Rändern und Aufteilen von Scheitel Punkten behandelt.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.

</dd> <dt>

*dwtextureinsemantic* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Eingabe Semantik der Textur Koordinate an. Wenn D3DX \_ Default ist, geht die Funktion davon aus, dass keine Texturkoordinaten vorhanden sind, und die Funktion schlägt fehl, es sei denn, die normale Vektor Berechnung wird angegeben.

</dd> <dt>

*dwtextureinindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn ein Mesh über mehrere Texturkoordinaten verfügt, gibt die Textur Koordinate an, die für die Tangens-Frame-Berechnungen verwendet werden soll. Wenn der Wert NULL ist, verfügt das Mesh nur über eine einzelne Textur Koordinate.

</dd> <dt>

*dwupartialoutsemantic* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Ausgabe Semantik für den Typ an, üblicherweise D3DDECLUSAGE \_ Tangens, der beschreibt, wo die partielle Ableitung in Bezug auf die U-Textur Koordinate gespeichert wird. Wenn D3DX den \_ Standardwert hat, wird diese partielle Ableitung nicht gespeichert.

</dd> <dt>

*dwupartialoutindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, bei dem die partielle Ableitung in Bezug auf die U-Textur Koordinate gespeichert werden soll.

</dd> <dt>

*dwvpartialoutsemantic* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den [**D3DDECLUSAGE**](./d3ddeclusage.md) -Typ an, in der Regel D3DDECLUSAGE \_ Binormal, der beschreibt, wo die partielle Ableitung in Bezug auf die V-Textur Koordinate gespeichert wird. Wenn D3DX den \_ Standardwert hat, wird diese partielle Ableitung nicht gespeichert.

</dd> <dt>

*dwvpartialoutindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, bei dem die partielle Ableitung in Bezug auf die V-Textur Koordinate gespeichert werden soll.

</dd> <dt>

*dwnormaloutsemantic* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die normale Semantik der Ausgabe an (normalerweise D3DDECLUSAGE normal), die \_ beschreibt, wo der normale Vektor bei jedem Scheitelpunkt gespeichert wird. Wenn D3DX den \_ Standardwert hat, wird dieser normale Vektor nicht gespeichert.

</dd> <dt>

*dwnormaloutindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, bei dem der normale Vektor in jedem Scheitelpunkt gespeichert werden soll.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [**D3DXTANGENT**](./d3dxtangent.md) -Flags, die Optionen für die Tangens Frame Berechnung angeben. Wenn der Wert **null** ist, werden die folgenden Optionen angegeben:



| BESCHREIBUNG                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Flagwert                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Gewichtung der normalen Vektor Länge um den Winkel im Bogenmaße, der von den beiden Kanten, die den Scheitelpunkt hinterlassen, untergeordneter Länge liegt. | &! (D3DXTANGENT \_ Gewichtung \_ nach \_ Bereich \| D3DXTANGENT \_ Gewichtung \_ gleich)                |
| Berechnen Sie orthogonale kartesische Koordinaten von Texturkoordinaten (u, v). Siehe Hinweise.                   | &! (D3DXTANGENT \_ Orthogonalize \_ from \_ U \| D3DXTANGENT \_ orthogonalize \_ from \_ V) |
| Texturen sind weder in der u-noch in der v-Richtung umschließt                                                     | &! (D3DXTANGENT \_ Wrapper \_ -UV)                                                      |
| Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.                                  | &! (D3DXTANGENT \_ \_ \_ partitionale nicht normalisieren                                     |
| Vertices werden um jedes Dreieck in der Richtung gegen den Uhrzeigersinn angeordnet.                               | &! (D3DXTANGENT \_ Wind- \_ CW)                                                      |
| Verwenden Sie die pro-Vertex-normal Vektoren, die bereits im Eingabe Mesh vorhanden sind.                                         | &! (D3DXTANGENT \_ \_normale berechnen)                                            |



 

Wenn D3DXTANGENT \_ Generate \_ on \_ Place nicht festgelegt ist, wird das eingabemesh geklont. Das ursprüngliche Mesh muss daher über ausreichend Speicherplatz verfügen, um den berechneten normalen Vektor und teilweise abgeleitete Daten zu speichern.

</dd> <dt>

*PDW-ency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt. Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) betragen.

</dd> <dt>

*' f '* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gibt den maximalen Kosinus des Winkels an, bei dem zwei partielle Ableitungen als nicht kompatibel eingestuft werden. Wenn das Punktprodukt der Richtung der beiden partiellen Ableitungen in angrenzenden Dreiecken kleiner oder gleich diesem Schwellenwert ist, werden die Scheitel Punkte, die von diesen Dreiecken gemeinsam genutzt werden, aufgeteilt.

</dd> <dt>

*' f ' (' f '* \[ ) in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Gibt die maximale Größe einer partiellen Ableitung an, bei der ein Scheitelpunkt als Singular eingestuft wird. Da mehrere Dreiecke an einem Punkt mit nahe gelegenen Tangenten Frames, aber vollständig abgebrochen werden (z. b. am oberen Rand einer Kugel), wird die Größe der partiellen Ableitung verringert. Wenn die Größe kleiner oder gleich diesem Schwellenwert ist, wird der Scheitelpunkt für jedes Dreieck aufgeteilt, das es enthält.

</dd> <dt>

" *Wert* \[ " in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Ähnlich wie bei fpartialedgethreshold gibt den maximalen Kosinus des Winkels zwischen zwei normalen an, bei denen es sich um einen Schwellenwert handelt, über den die von Dreiecken gemeinsam genutzten Scheitel Punkte aufgeteilt werden. Wenn das Punktprodukt der beiden normale kleiner als der Schwellenwert ist, werden die freigegebenen Scheitel Punkte aufgeteilt und bilden einen festen Rand zwischen benachbarten Dreiecken. Wenn das Punktprodukt den Schwellenwert überschreitet, werden die normalen der benachbarten Dreiecke interpoliert.

</dd> <dt>

*ppmeshout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Adresse eines Zeigers auf ein Output [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, das die berechneten Tangens-, Binormale-und normal Vektordaten empfängt.

</dd> <dt>

*ppvertexmapping* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Adresse eines Zeigers auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Ausgabepuffer Objekt, das eine Zuordnung von neuen Scheitel Punkten empfängt, die von dieser Methode in den ursprünglichen Scheitel Punkten berechnet werden. Der Puffer ist ein Array von DWords, wobei die Array Größe als Anzahl von Vertices in ppmeshout definiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Eine vereinfachte Version dieser Funktion ist als [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)verfügbar.

Der berechnete normale Vektor bei jedem Scheitelpunkt wird immer normalisiert, sodass er über eine Einheitslänge verfügt.

Die stabilste Lösung für die Berechnung von orthogonalen kartesischen Koordinaten ist das Festlegen von Flags D3DXTANGENT \_ orthogonalize \_ von \_ Ihnen und D3DXTANGENT \_ orthogonalize \_ von \_ v, sodass orthogonale Koordinaten sowohl aus den Texturkoordinaten Sie als auch mit v berechnet werden. Wenn in diesem Fall jedoch entweder "u" oder "v" gleich NULL ist, berechnet die Funktion orthogonale Koordinaten mithilfe von D3DXTANGENT \_ orthogonalize \_ von \_ v bzw \_ . D3DXTANGENT orthogonalize \_ von \_ u bzw..

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
