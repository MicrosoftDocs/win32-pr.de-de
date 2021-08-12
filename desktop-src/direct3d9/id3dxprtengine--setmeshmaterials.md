---
description: Legt Gittermaterialeigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Unterflächens scattering-Parameter anzugeben.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: ID3DXPRTEngine::SetMeshMaterials-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c24ff96b4582e86580774a1f7ac7cd889547018a5b0f138d5e43685c50e1701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293384"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>ID3DXPRTEngine::SetMeshMaterials-Methode

Legt Gittermaterialeigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Unterflächens scattering-Parameter anzugeben.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppMaterials* \[ In\]
</dt> <dd>

Typ: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Adresse eines Zeigers auf gewünschte Gittermaterialeigenschaften. Siehe [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*NumMeshes* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Index des Gitternetzes, für das Materialeigenschaften festgelegt werden sollen.

</dd> <dt>

*NumChannels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Farbkanäle, die im Gitternetz festgelegt werden sollen. Legen Sie auf 1 fest, um graue Materialien anzugeben (R = G = B) oder 3, um Farbunterdärkungseffekte zu ermöglichen. Wenn Sie diesen Parameter ändern möchten, legen Sie zuerst den Albedo mithilfe einer anderen Methode fest, z.B. [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) oder [**ID3DXPRTEngine::SetPerVertexAlbedo.**](id3dxprtengine--setpervertexalbedo.md)

</dd> <dt>

*bSetAlbedo* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True gibt an, dass der Albedo des Gitternetzes auf ppMaterials festgelegt wird, wobei alle vorhandenen Texel- und Scheitelpunkt-Albedowerte überschrieben werden. False gibt an, dass alle vorhandenen Texel- und Scheitelpunkt-Albedo-Werte beibehalten werden, die von anderen Methoden festgelegt wurden. NumChannels muss mit dem NumChannels-Parameter übereinstimmen, der zum Erstellen des Puffers in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) oder [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)verwendet wird.

</dd> <dt>

*fLengthScale* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Skalierung der 3D-Szene relativ zu einem 1-mm-Würfel. Wird für Berechnungen von Punktdiagrammen unter der Oberfläche verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
