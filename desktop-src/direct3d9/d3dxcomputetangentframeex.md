---
description: Führt Tangensframeberechnungen für ein Gitternetz aus. Tangens-, binormale und optional normale Vektoren werden generiert. Singularitäten werden nach Bedarf durch Gruppieren von Kanten und Teilen von Scheitelpunkt behandelt.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: D3DXComputeTangentFrameEx-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988670"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx-Funktion

Führt Tangensframeberechnungen für ein Gitternetz aus. Tangens-, binormale und optional normale Vektoren werden generiert. Singularitäten werden nach Bedarf durch Gruppieren von Kanten und Teilen von Scheitelpunkt behandelt.

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

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\***

Zeiger auf ein [**Eingabe-ID3DXMesh-Gittermodellobjekt.**](id3dxmesh.md)

</dd> <dt>

*dwTextureInSemantic* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Semantik der Texturkoordinateneingabe an. Bei D3DX DEFAULT geht die Funktion davon aus, dass keine Texturkoordinaten enthalten sind, und die Funktion kann nur dann fehlschlagen, wenn \_ eine normale Vektorberechnung angegeben ist.

</dd> <dt>

*dwTextureInIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wenn ein Gitternetz über mehrere Texturkoordinaten verfügt, gibt die Texturkoordinate an, die für die Tangensframeberechnungen verwendet werden soll. Wenn 0 (null) ist, hat das Gitternetz nur eine einzelne Texturkoordinate.

</dd> <dt>

*dwUPartialOutSemantic* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Ausgabesemantik für den Typ an, in der Regel D3DDECLUSAGE TANGENT, der beschreibt, wo die partielle Ableitung in Bezug auf die U-Texturkoordinate \_ gespeichert wird. Bei D3DX \_ DEFAULT wird diese partielle Ableitung nicht gespeichert.

</dd> <dt>

*dwUPartialOutIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, an dem die partielle Ableitung in Bezug auf die U-Texturkoordinate gespeichert werden soll.

</dd> <dt>

*dwVPartialOutSemantic* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den [**D3DDECLUSAGE-Typ**](./d3ddeclusage.md) an, in der Regel D3DDECLUSAGE BINORMAL, der beschreibt, wo die partielle Ableitung in Bezug auf die V-Texturkoordinate \_ gespeichert wird. Bei D3DX \_ DEFAULT wird diese partielle Ableitung nicht gespeichert.

</dd> <dt>

*dwVPartialOutIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, an dem die partielle Ableitung in Bezug auf die V-Texturkoordinate gespeichert werden soll.

</dd> <dt>

*dwNormalOutSemantic* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die normale Ausgabesemantik an, in der Regel D3DDECLUSAGE NORMAL, die beschreibt, wo der normale Vektor an jedem Scheitelpunkt \_ gespeichert wird. Bei D3DX \_ DEFAULT wird dieser normale Vektor nicht gespeichert.

</dd> <dt>

*dwNormalOutIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den semantischen Index an, an dem der normale Vektor an jedem Scheitelpunkt gespeichert werden soll.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von mindestens einem [**D3DXTANGENT-Flag,**](./d3dxtangent.md) das Tangensframe-Berechnungsoptionen an angeben. Bei **NULL** werden die folgenden Optionen angegeben:



| Beschreibung                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Flagwert                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Gewichten Sie die normale Vektorlänge nach dem Winkel im Bogenmaß, der von den beiden Kanten, die den Scheitelpunkt verlassen, unterstützt wird. | & ! ( D3DXTANGENT \_ GEWICHTUNG \_ \_ NACH BEREICH \| D3DXTANGENT \_ \_ GEWICHTUNG GLEICH )                |
| Berechnen Sie orthogonale kartesische Koordinaten aus Texturkoordinaten (u, v). Siehe Hinweise.                   | & ! ( D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U \| D3DXTANGENT \_ ORTHOGONALIZE \_ FROM V \_ ) |
| Texturen sind weder in u- noch in v-Richtungen umschlossen.                                                     | & ! ( D3DXTANGENT \_ WRAP \_ UV )                                                      |
| Partielle Ableitungen in Bezug auf Texturkoordinaten werden normalisiert.                                  | & ! ( D3DXTANGENT \_ DONT \_ NORMALIZE \_ PARTIALS )                                     |
| Scheitelpunkts werden gegen den Uhrzeigersinn um jedes Dreieck herum geordnet.                               | & ! ( D3DXTANGENT \_ WIND \_ CW )                                                      |
| Verwenden Sie normale Vektoren pro Scheitelpunkt, die bereits im Eingabegitternetz vorhanden sind.                                         | & ! ( D3DXTANGENT \_ CALCULATE \_ NORMALS )                                            |



 

Wenn D3DXTANGENT \_ GENERATE IN PLACE nicht festgelegt \_ \_ ist, wird das Eingabegitternetz geklont. Das ursprüngliche Gitternetz muss daher über ausreichend Speicherplatz verfügen, um den berechneten normaler Vektor und partielle abgeleitete Daten zu speichern.

</dd> <dt>

*pdwAdjacency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD) betragen.

</dd> <dt>

*fPartialEdgeThreshold* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt den maximalen Kosinus des Winkels an, bei dem zwei partielle Ableitungen als inkompatibel angesehen werden. Wenn das Punktprodukt der Richtung der beiden partiellen Ableitungen in angrenzenden Dreiecken kleiner oder gleich diesem Schwellenwert ist, werden die Scheitelpunkte, die von diesen Dreiecken gemeinsam genutzt werden, aufgeteilt.

</dd> <dt>

*fSingularPointThreshold* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt die maximale Größe einer partiellen Ableitung an, bei der ein Scheitelpunkt als singular betrachtet wird. Da mehrere Dreiecke an einem Punkt mit tangensischen Rahmen in der Nähe liegen, sich jedoch vollständig gegenseitig abbrechen (z. B. am Oberen einer Kugel), nimmt die Größe der partiellen Ableitung ab. Wenn die Größe kleiner oder gleich diesem Schwellenwert ist, wird der Scheitelpunkt für jedes Dreieck aufgeteilt, das ihn enthält.

</dd> <dt>

*fNormalEdgeThreshold* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ähnlich wie fPartialEdgeThreshold gibt den maximalen Kosinus des Winkels zwischen zwei Normals an, bei dem es sich um einen Schwellenwert handelt, über den scheiteltische Punkte, die von Dreiecken gemeinsam genutzt werden, aufgeteilt werden. Wenn das Punktprodukt der beiden Normalwerte kleiner als der Schwellenwert ist, werden die freigegebenen Scheitelpunkte aufgeteilt und bilden eine harte Kante zwischen benachbarten Dreiecken. Wenn das Punktprodukt größer als der Schwellenwert ist, werden benachbarte Dreiecke normal interpoliert.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Adresse eines Zeigers auf ein [**Ausgabe-ID3DXMesh-Gittermodellobjekt,**](id3dxmesh.md) das die berechneten Tangens-, binormalen und normalen Vektordaten empfängt.

</dd> <dt>

*ppVertexMapping* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Adresse eines Zeigers auf ein [**Ausgabe-ID3DXBuffer-Pufferobjekt,**](id3dxbuffer.md) das eine Zuordnung neuer Scheitelpunkts empfängt, die von dieser Methode zu den ursprünglichen Scheitelpunkts berechnet werden. Der Puffer ist ein Array von DWORDs, bei dem die Arraygröße als Anzahl von Scheitelzeichen in ppMeshOut definiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Eine vereinfachte Version dieser Funktion ist als [**D3DXComputeTangentFrame verfügbar.**](d3dxcomputetangentframe.md)

Der berechnete Normalvektor an jedem Scheitelpunkt wird immer normalisiert, um eine Einheitenlänge zu haben.

Die stabilste Lösung für die Berechnung von orthogonalen kartesischen Koordinaten besteht im Festlegen der Flags D3DXTANGENT \_ ORTHOGONALIZE FROM you und \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, sodass \_ \_ orthogonale Koordinaten aus beiden Texturkoordinaten von Ihnen und v berechnet werden. In diesem Fall berechnet die Funktion jedoch mithilfe von D3DXTANGENT ORTHOGONALIZE FROM V bzw. \_ \_ \_ D3DXTANGENT ORTHOGONALIZE FROM U or D3DXTANGENT \_ ORTHOGONALIZE FROM U orthogonalale \_ Koordinaten, wenn u oder v 0 (null) \_ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
