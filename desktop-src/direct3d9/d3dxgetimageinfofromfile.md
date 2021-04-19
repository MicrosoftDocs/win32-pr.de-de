---
description: Ruft Informationen zu einer angegebenen Bilddatei ab.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: D3DXGetImageInfoFromFile-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361205"
---
# <a name="d3dxgetimageinfofromfile-function"></a>D3DXGetImageInfoFromFile-Funktion

Ruft Informationen zu einer angegebenen Bilddatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psrcfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Dateiname des Bilds, über das Informationen abgerufen werden sollen. Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.

</dd> <dt>

*psrcinfo* \[ in\]
</dt> <dd>

Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***

Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
