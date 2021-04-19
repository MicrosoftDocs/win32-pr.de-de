---
description: Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart. Beachten Sie, dass Sie anstelle der Verwendung dieser Funktion DirectWrite und die directxtk-Bibliothek, spritefont-Klasse, verwenden.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: D3DX10CreateFont-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367380"
---
# <a name="d3dx10createfont-function"></a>D3DX10CreateFont-Funktion

Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart.

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfehlen wir die Verwendung von [DirectWrite](../directwrite/direct-write-portal.md) und der [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek, **spritefont** Class.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf eine ID3D10Device-Schnittstelle, das Gerät, das dem Schriftart Objekt zugeordnet werden soll.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

Die Höhe der Zeichen in logischen Einheiten.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Breite der Zeichen in logischen Einheiten.

</dd> <dt>

*Gewichtung* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Schrift Breite. Ein Beispiel ist "Bold".

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl von MipMap-Ebenen.

</dd> <dt>

*Kursiv* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

True für kursiv Schrift, andernfalls false.

</dd> <dt>

Zeichen *Satz* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Zeichensatz der Schriftart.

</dd> <dt>

*Outputprecision* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Gibt an, wie Windows versuchen soll, die gewünschten Schriftgrößen und Merkmale mit tatsächlichen Schriftarten abzugleichen. Verwenden \_ \_ \_ Sie nur die Precis-präcis, um sicherzustellen, dass Sie immer eine TrueType-Schriftart erhalten.

</dd> <dt>

*Qualität* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Gibt an, wie Windows der gewünschten Schriftart mit einer echten Schriftart entsprechen soll. Sie gilt nur für Raster Schriftarten und sollte sich nicht auf TrueType-Schriftarten auswirken.

</dd> <dt>

*PitchAndFamily* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der-und der-Familien Index.

</dd> <dt>

*pfakename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Namen der Schriftart enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*ppfont* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Gibt einen Zeiger auf eine ID3DX10Font-Schnittstelle zurück, die das erstellte Schriftart Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateFontA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Weitere Informationen zu Schriftart Parametern finden Sie in [der logischen Schriftart](/previous-versions//ms533985(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
