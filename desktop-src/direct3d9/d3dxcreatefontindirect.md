---
description: Erstellt ein Schriftart Objekt indirekt für ein Gerät und eine Schriftart.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: D3DXCreateFontIndirect-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355457"
---
# <a name="d3dxcreatefontindirect-function"></a>D3DXCreateFontIndirect-Funktion

Erstellt ein Schriftart Objekt indirekt für ein Gerät und eine Schriftart.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das dem Schriftart Objekt zugeordnet werden soll.

</dd> <dt>

*PDE SC* \[ in\]
</dt> <dd>

Typ: **[**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Ein Zeiger auf eine [**D3DXFONT \_ -Struktur**](d3dxfont-desc.md) , die die Attribute des zu erstellenden Schriftart Objekts beschreibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp D3DXFONT \_ DESC in D3DXFONT \_ descw aufgelöst; andernfalls wird der Datentyp in D3DXFONT \_ DeScA aufgelöst. Siehe Hinweise.

</dd> <dt>

*ppfont* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***

Gibt einen Zeiger auf eine [**ID3DXFont**](id3dxfont.md) -Schnittstelle zurück, die das erstellte Schriftart Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontIndirectW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateFontIndirectA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
