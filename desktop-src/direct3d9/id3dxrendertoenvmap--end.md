---
description: Stellen Sie alle Renderziele wieder her, und erstellen Sie bei Bedarf alle gerenderten Gesichter in der Umgebungszuordnungsoberfläche.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: ID3DXRenderToEnvMap::End-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efaf32eb421f6bda38fb922c4a89b1dbbe871842c3b4f07a87ff30c2e6b4dc40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095790"
---
# <a name="id3dxrendertoenvmapend-method"></a>ID3DXRenderToEnvMap::End-Methode

Stellen Sie alle Renderziele wieder her, und erstellen Sie bei Bedarf alle gerenderten Gesichter in der Umgebungszuordnungsoberfläche.

## <a name="syntax"></a>Syntax


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine gültige Kombination aus einem oder mehreren [D3DX-FILTER-Flags. \_ ](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
