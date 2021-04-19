---
description: Speichert eine Textur im Speicher.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: D3DX10SaveTextureToMemory-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370428"
---
# <a name="d3dx10savetexturetomemory-function"></a>D3DX10SaveTextureToMemory-Funktion

Speichert eine Textur im Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Zeiger auf die zu speichernde Textur. Siehe [**ID3D10Resource-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*Destformat* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**

Das Format, in dem die Textur gespeichert wird. Siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).

</dd> <dt>

*ppdestbuf* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf den Speicher, der die gespeicherte Textur enthält. Siehe [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Dies ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
