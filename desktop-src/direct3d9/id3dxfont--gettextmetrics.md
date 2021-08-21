---
description: Ruft Schriftartmerkmale ab, die in einer TEXTMETRIC-Struktur identifiziert werden. Diese Methode unterstützt ANSI- und Unicode-Compilereinstellungen.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: ID3DXFont::GetTextMetrics-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9254ec9d5224f9041079f36bc95d68ea7346cf6dac2aecb81e7a6009496675e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987410"
---
# <a name="id3dxfontgettextmetrics-method"></a>ID3DXFont::GetTextMetrics-Methode

Ruft Schriftartmerkmale ab, die in einer [**TEXTMETRIC-Struktur identifiziert**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) werden. Diese Methode unterstützt ANSI- und Unicode-Compilereinstellungen.

## <a name="syntax"></a>Syntax


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTextMetrics* \[ out\]
</dt> <dd>

Typ: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Zeiger auf eine [**TEXTMETRIC-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) die Schriftarteigenschaften enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, gibt die Funktion eine TEXTMETRICW-Struktur zurück. Andernfalls gibt der Funktionsaufruf eine TEXTMETRICA-Struktur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
