---
description: Erstellt ein Schriftart Objekt. Beachten Sie, dass Sie anstelle der Verwendung dieser Funktion DirectWrite und die directxtk-Bibliothek, spritefont-Klasse, verwenden.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: D3DX10CreateFontIndirect-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354486"
---
# <a name="d3dx10createfontindirect-function"></a>D3DX10CreateFontIndirect-Funktion

Erstellt ein Schriftart Objekt.

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfehlen wir die Verwendung von [DirectWrite](../directwrite/direct-write-portal.md) und der [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek, **spritefont** Class.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf eine [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstelle.

</dd> <dt>

*PDE SC* \[ in\]
</dt> <dd>

Typ: **Konstanten [**d3dx10 \_ Schriftart \_ DESC**](d3dx10-font-desc.md) \***

Ein Zeiger auf [**eine \_ d3dx10 \_ Font**](d3dx10-font-desc.md) -Struktur, die die Attribute des zu erstellenden Schriftart Objekts beschreibt. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontIndirectW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateFontIndirectA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

</dd> <dt>

*ppfont* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Gibt einen Zeiger auf eine [**ID3DX10Font-Schnittstelle**](id3dx10font.md)zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
