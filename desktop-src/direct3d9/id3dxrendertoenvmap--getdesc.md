---
description: Ruft die Beschreibung der Renderoberfläche ab.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap:: getdesc-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761997"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>ID3DXRenderToEnvMap:: getdesc-Methode

Ruft die Beschreibung der Renderoberfläche ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Zeiger auf eine [**D3DXRTE \_**](d3dxrte-desc.md) -Struktur, die die Renderingoberfläche beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




