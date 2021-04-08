---
description: Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: D3DXCreateFont-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762192"
---
# <a name="d3dxcreatefont-function"></a>D3DXCreateFont-Funktion

Erstellt ein Schriftart Objekt für ein Gerät und eine Schriftart.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das dem Schriftart Objekt zugeordnet werden soll.

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

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Zeichensatz der Schriftart.

</dd> <dt>

*Outputprecision* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt an, wie Windows versuchen soll, die gewünschten Schriftgrößen und Merkmale mit tatsächlichen Schriftarten abzugleichen. Verwenden \_ \_ \_ Sie nur die Precis-präcis, um sicherzustellen, dass Sie immer eine TrueType-Schriftart erhalten.

</dd> <dt>

*Qualität* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt an, wie Windows der gewünschten Schriftart mit einer echten Schriftart entsprechen soll. Sie gilt nur für Raster Schriftarten und sollte sich nicht auf TrueType-Schriftarten auswirken.

</dd> <dt>

*PitchAndFamily* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der-und der-Familien Index.

</dd> <dt>

*pfakename* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Namen der Schriftart enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*ppfont* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***

Gibt einen Zeiger auf eine [**ID3DXFont**](id3dxfont.md) -Schnittstelle zurück, die das erstellte Schriftart Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Erstellung eines ID3DXFont-Objekts erfordert, dass das Gerät 32-Bit-Farbe unterstützt.

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateFontW aufgelöst. Andernfalls wird der Funktions Aufruhe in D3DXCreateFontA aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Weitere Informationen zu Schriftart Parametern finden Sie in [der logischen Schriftart](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
