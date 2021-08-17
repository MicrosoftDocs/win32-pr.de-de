---
description: 'ID3DXTextureShader::GetDesc-Methode: Ruft eine Beschreibung der konstanten Tabelle ab.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: ID3DXTextureShader::GetDesc-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06619730ceaa03dfdc812c669726bcde032caf7380ce4a7736085ee3a62b9d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729023"
---
# <a name="id3dxtextureshadergetdesc-method"></a>ID3DXTextureShader::GetDesc-Methode

Ruft eine Beschreibung der konstanten Tabelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***

Die Attribute der konstanten Tabelle. Siehe [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




