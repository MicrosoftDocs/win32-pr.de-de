---
description: 'ID3DX10Mesh::Optimize-Methode: Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelpunkten, um die Zeichnungsleistung zu optimieren.'
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
ms.openlocfilehash: 41bc7b4ac7fb263073a88cd998190b0fa6e044d528f9d3f4613c3284f28c0f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302575"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh::Optimize-Methode

Generiert ein neues Gitternetz mit neu angeordneten Gesichtern und Scheitelpunkten, um die Zeichnungsleistung zu optimieren.

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

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt den Typ der auszuführenden Optimierung an. Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus D3DXMESHOPT und D3DXMESH festgelegt werden (mit Ausnahme von D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY und D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Array von UINTs , eins pro Gesicht, das das ursprüngliche Gitternetz identifiziert, das den einzelnen Gesichtern im optimierten Gitternetz entspricht. Wenn der für dieses Argument angegebene Wert **NULL** ist, werden keine Gesichtszuordnungsdaten zurückgegeben.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf eine [**ID3D10Blob-Schnittstelle,**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitelpunkte den alten Scheitelpunkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunktzuordnung ändern müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Diese Methode generiert ein neues Gitternetz. Vor dem Ausführen von Optimize muss eine Anwendung einen Adjazenzpuffer generieren, indem [**ID3DX10Mesh::GenerateAdjaencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)aufgerufen wird. Der Adjazenzpuffer enthält Adjazenzdaten, z. B. eine Liste von Kanten und den nebeneinander liegenden Gesichtern.

Diese Methode ist der [**ID3DX10Mesh::CloneMesh-Methode**](id3dx10mesh-clonemesh.md) sehr ähnlich, mit der Ausnahme, dass sie beim Generieren des neuen Klons des Gitternetzes Optimierungen ausführen kann. Das Ausgabegitternetz erbt alle Erstellungsparameter des Eingabegitters.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
