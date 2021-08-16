---
description: Erstellt ein Schriftartobjekt für ein Gerät und eine Schriftart.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: D3DXCreateFont-Funktion (D3dx9core.h)
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
ms.openlocfilehash: d9bac71e89657f4df176a1ee15e2dca0cda6e4a25b8c47560adc5cf26c982383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526154"
---
# <a name="d3dxcreatefont-function"></a>D3DXCreateFont-Funktion

Erstellt ein Schriftartobjekt für ein Gerät und eine Schriftart.

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Gerät, das dem Schriftartobjekt zugeordnet werden soll.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Die Höhe der Zeichen in logischen Einheiten.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Breite der Zeichen in logischen Einheiten.

</dd> <dt>

*Gewichtung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Schriftgewichtung. Ein Beispiel ist fett.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Mipmap-Ebenen.

</dd> <dt>

*Italisch* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True für die italische Schriftart, andernfalls FALSE.

</dd> <dt>

*CharSet* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Zeichensatz der Schriftart.

</dd> <dt>

*OutputPrecision* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt an, Windows, wie versucht werden soll, die gewünschten Schriftgrößen und -merkmale mit den tatsächlichen Schriftarten zu finden. Verwenden Sie \_ beispielsweise OUT TT ONLY PRECIS, um sicherzustellen, dass Sie immer eine \_ \_ TrueType-Schriftart erhalten.

</dd> <dt>

*Qualität* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt an, Windows der gewünschten Schriftart mit einer echten Schriftart übereinstimmen soll. Sie gilt nur für Rasterschriftarten und sollte sich nicht auf TrueType-Schriftarten auswirken.

</dd> <dt>

*PitchAndFamily* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Tonhöhe und Familienindex.

</dd> <dt>

*pFacename* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Schriftartnamen enthält. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXFONT**](id3dxfont.md)\***

Gibt einen Zeiger auf eine [**ID3DXFont-Schnittstelle**](id3dxfont.md) zurück, die das erstellte Schriftartobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Erstellung eines ID3DXFont-Objekts erfordert, dass das Gerät 32-Bit-Farben unterstützt.

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateFontW auflösen. Andernfalls wird der Funktionsaufruf in D3DXCreateFontA auflösen, da ANSI-Zeichenfolgen verwendet werden.

Weitere Informationen zu Schriftartparametern finden Sie unter [Die logische Schriftart](../gdi/creating-a-logical-font.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
