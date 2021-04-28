---
description: 'D3DXGetImageInfoFromFile-Funktion: Ruft Informationen zu einer bestimmten Bilddatei ab.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: D3DXGetImageInfoFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114493"
---
# <a name="d3dxgetimageinfofromfile-function"></a>D3DXGetImageInfoFromFile-Funktion

Ruft Informationen zu einer bestimmten Bilddatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Dateiname des Bilds, zu dem Informationen abgerufen werden. Wenn UNICODE oder UNICODE definiert sind, ist dieser \_ Parametertyp LPCWSTR, andernfalls ist der Typ LPCSTR.

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Bemerkungen

Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
