---
description: Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762042"
---
# <a name="d3dxgetimageinfofromresource-function"></a>D3DXGetImageInfoFromResource-Funktion

Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.

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

*hsrcmodule* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Das Modul, in dem die Ressource geladen wird. Legen Sie diesen Parameter auf **null** fest, um das Modul anzugeben, das dem Image zugeordnet ist, das vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.

</dd> <dt>

*psrcfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

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

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXGetImageInfoFromResourceW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXGetImageInfoFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
