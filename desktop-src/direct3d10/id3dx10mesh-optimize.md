---
description: 'ID3DX10Mesh::Optimize-Methode: Generiert ein neues Gitter mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: ID3DX10Mesh::Optimize-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108048"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh::Optimize-Methode

Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelungen, um die Zeichnungsleistung zu optimieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt den Typ der durchzuführenden Optimierung an. Dieser Parameter kann auf eine Kombination aus mindestens einem Flag von D3DXMESHOPT und D3DXMESH festgelegt werden (außer D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY und D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Array von UINTs pro Gesicht, das das ursprüngliche Gitternetzgesicht identifiziert, das jedem Gesicht im optimierten Gitter entspricht. Wenn der für dieses Argument angegebene Wert **NULL ist,** werden keine Gesichtszuordnungsdaten zurückgegeben.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf eine [**ID3D10Blob-Schnittstelle,**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)die ein DWORD für jeden Scheitelpunkt enthält, das angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkte zuordnen. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert ein neues Gitter. Vor dem Ausführen von Optimize muss eine Anwendung durch Aufrufen von [**ID3DX10Mesh::GenerateAdjacencyAndPointReps einen Adjacency-Puffer generieren.**](id3dx10mesh-generateadjacencyandpointreps.md) Der Adjacency-Puffer enthält Adjacency-Daten, z. B. eine Liste von Kanten und die nebeneinander liegenden Gesichter.

Diese Methode ist der [**ID3DX10Mesh::CloneMesh-Methode**](id3dx10mesh-clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitternetzes Optimierungen ausführen kann. Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
