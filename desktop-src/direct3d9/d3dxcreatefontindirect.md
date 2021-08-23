---
description: Erstellt indirekt ein Schriftartobjekt für ein Gerät und eine Schriftart.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: D3DXCreateFontIndirect-Funktion (D3dx9core.h)
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
ms.openlocfilehash: 555c4b1f3615639d9da01fb7a2a96aa5cb15f697235c918d5130ffcd4d43baa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988660"
---
# <a name="d3dxcreatefontindirect-function"></a>D3DXCreateFontIndirect-Funktion

Erstellt indirekt ein Schriftartobjekt für ein Gerät und eine Schriftart.

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Gerät, das dem Schriftartobjekt zugeordnet werden soll.

</dd> <dt>

*pDesc* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Zeiger auf eine [**D3DXFONT \_ DESC-Struktur,**](d3dxfont-desc.md) die die Attribute des zu erstellenden Schriftartobjekts beschreibt. Wenn die Compilereinstellungen Unicode erfordern, wird der D3DXFONT DESC-Datentyp in D3DXFONT DESCW auflösen. Andernfalls wird der Datentyp in \_ \_ D3DXFONT \_ DESCA auflösen. Siehe Hinweise.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***

Gibt einen Zeiger auf eine [**ID3DXFont-Schnittstelle**](id3dxfont.md) zurück, die das erstellte Schriftartobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateFontIndirectW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateFontIndirectA auflösen, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
