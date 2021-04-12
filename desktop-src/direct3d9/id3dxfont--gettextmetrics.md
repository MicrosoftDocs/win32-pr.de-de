---
description: Ruft Schriftart Eigenschaften ab, die in einer TextMetric-Struktur identifiziert werden. Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont:: GetTextMetrics-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354766"
---
# <a name="id3dxfontgettextmetrics-method"></a>ID3DXFont:: GetTextMetrics-Methode

Ruft Schriftart Eigenschaften ab, die in einer [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) -Struktur identifiziert werden. Diese Methode unterstützt die ANSI-und Unicode-Compilereinstellungen.

## <a name="syntax"></a>Syntax


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptextmetrics* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Zeiger auf eine [**textmetrikstruktur**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , die Schriftart Eigenschaften enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, gibt die Funktion eine textmetricw-Struktur zurück. Andernfalls gibt der Funktions Aufruhe eine textmetrica-Struktur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
