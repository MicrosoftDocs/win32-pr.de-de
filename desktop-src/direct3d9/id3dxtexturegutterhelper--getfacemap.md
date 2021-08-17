---
description: Ruft den Index der Gitternetzgesicht ab, zu der jedes Texel gehört.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: ID3DXTextureGutterHelper::GetFaceMap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5fce4400b1f778581f830fff60ef4e1519ad73752da02f5194abe64f433d43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729189"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>ID3DXTextureGutterHelper::GetFaceMap-Methode

Ruft den Index der Gitternetzgesicht ab, zu der jedes Texel gehört.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFaceData* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf den Index der Gitternetzgesicht, zu der jedes Texel gehört.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Die von dieser Methode zurückgegebenen Mesh-Gesichtserkennungsdaten sind nur für gültige Texel (nicht der Klasse 0) gültig. [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texel (keine Klasse 0) zurück.

Bei [**Texeln der Klasse 2**](id3dxtexturegutterhelper.md)ruft diese Methode das nächstgelegene Gesicht ab.

Die Anwendung muss pFaceData zuordnen und verwalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
