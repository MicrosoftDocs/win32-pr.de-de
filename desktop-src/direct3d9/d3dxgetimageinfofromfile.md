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
ms.openlocfilehash: 1726fae1697a48d8e4aa406f5eb5cec03f6071fed4b36a199b10e385a24e6249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027630"
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

Dateiname des Bilds, zu dem Informationen abgerufen werden sollen. Wenn UNICODE oder \_ UNICODE definiert ist, ist dieser Parametertyp LPCWSTR, andernfalls LPCSTR.

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
