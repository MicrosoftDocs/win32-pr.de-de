---
description: Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'ID3DXRenderToEnvMap:: Face-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762345"
---
# <a name="id3dxrendertoenvmapface-method"></a>ID3DXRenderToEnvMap:: Face-Methode

Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* \[ in\]
</dt> <dd>

Typ: **[ **D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md)**

Das erste Gesicht der Umgebungs Cube-Karte. Siehe [**D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine gültige Kombination aus einem oder mehreren [D3DX- \_ Filterflags](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss für jeden Typ von Umgebungs Zuordnung einmal aufgerufen werden. Die einzige Ausnahme ist eine kubische Umgebungs Zuordnung, die erfordert, dass diese Methode sechs Mal aufgerufen wird, einmal für jedes Gesicht in D3DCUBEMAP \_ Gesichter. Weitere Informationen finden Sie unter [Umgebungs Zuordnung (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
