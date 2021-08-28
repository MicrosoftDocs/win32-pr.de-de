---
description: Ruft die Beschreibung der Renderoberfläche ab.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: ID3DXRenderToEnvMap::GetDesc-Methode (D3dx9core.h)
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
ms.openlocfilehash: 7cfe9f3e8e857806895ec8be249d51f63ffe4818f24bbbf12d842754a885e855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847304"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>ID3DXRenderToEnvMap::GetDesc-Methode

Ruft die Beschreibung der Renderoberfläche ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Zeiger auf eine [**D3DXRTE \_ DESC-Struktur,**](d3dxrte-desc.md) die die Renderingoberfläche beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




