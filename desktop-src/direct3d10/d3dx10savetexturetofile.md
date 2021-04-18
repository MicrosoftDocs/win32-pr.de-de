---
description: Speichert eine Textur in einer Datei.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: D3DX10SaveTextureToFile-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351997"
---
# <a name="d3dx10savetexturetofile-function"></a>D3DX10SaveTextureToFile-Funktion

Speichert eine Textur in einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
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

Das Format, in dem die Textur gespeichert wird (siehe [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)). D3dx10 \_ IFF \_ DDS ist das bevorzugte Format, da es die einzige Option ist, die alle Formate im [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)unterstützt.

</dd> <dt>

*pdestfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Der Name der Ziel Ausgabedatei, in der die Textur gespeichert wird. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind. Verwenden Sie den Rückgabewert, um festzustellen, ob *destformat* unterstützt wird.

## <a name="remarks"></a>Bemerkungen

**D3DX10SaveTextureToFile** schreibt die zusätzliche [**DDS- \_ Header \_ DXT10**](../direct3ddds/dds-header-dxt10.md) -Struktur nur bei Bedarf für die Eingabe Textur (z. b. weil die Eingabe Textur im Standard-RGB-Format (sRGB) vorliegt). Wenn **D3DX10SaveTextureToFile** die **DDS- \_ Header \_ DXT10** -Struktur ausgibt, wird der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](../direct3ddds/dds-pixelformat.md) -Struktur für die Textur auf **DX10** festgelegt, um die präscense des **DDS- \_ Headers \_ DXT10** Extended-Header anzugeben.

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

 

 
