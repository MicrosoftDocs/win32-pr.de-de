---
description: Legt gittermaterial Eigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Parameter für die unter Surface-Verteilung anzugeben.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine:: stmeschmaterials-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355686"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>ID3DXPRTEngine:: stmeschmaterials-Methode

Legt gittermaterial Eigenschaften in der 3D-Szene fest. Verwenden Sie diese Methode, um Parameter für die unter Surface-Verteilung anzugeben.

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

*ppmaterials* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Adresse eines Zeigers auf gewünschte gittermaterial Eigenschaften. Siehe [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*Nummeshes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Index des Netzes, in dem Materialeigenschaften festgelegt werden sollen.

</dd> <dt>

*Numchannels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Farbkanälen, die im Mesh festgelegt werden sollen. Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren. Wenn Sie diesen Parameter ändern möchten, legen Sie zuerst "Albedo" mit einer anderen Methode fest, wie z. [**b. ID3DXPRTEngine:: setpertexelalbedo**](id3dxprtengine--setpertexelalbedo.md) oder [**ID3DXPRTEngine:: setpervertexalbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*babtalbedo* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Wenn **true**, wird die Albedo-Option des Netzes auf ppmaterials festgelegt, wobei alle vorhandenen texelwerte und Vertex-Albedo-Werte überschrieben werden. Wenn **false**, werden alle vorhandenen texkingwerte und Vertex Albedo-Werte beibehalten, die von anderen Methoden festgelegt werden. Numchannels muss mit dem Parameter numchannels identisch sein, der zum Erstellen des Puffers in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) oder [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)verwendet wird.

</dd> <dt>

*flengthscale* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Skalierung der 3D-Szene in Relation zu einem 1-mm-Cube. Wird für die Berechnung von subsurface-Strukturen verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
