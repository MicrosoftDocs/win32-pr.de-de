---
description: 'D3DXGetImageInfoFromResource-Funktion: Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.'
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114448"
---
# <a name="d3dxgetimageinfofromresource-function"></a>D3DXGetImageInfoFromResource-Funktion

Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Modul, in das die Ressource geladen wird. Legen Sie diesen Parameter auf **NULL fest,** um das Modul anzugeben, das dem Image zugeordnet ist, das das Betriebssystem zum Erstellen des aktuellen Prozesses verwendet hat.

</dd> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

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

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXGetImageInfoFromResourceW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXGetImageInfoFromResourceA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
