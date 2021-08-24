---
title: IDWriteFontFace GetGdiCompatibleMetrics-Methode
description: Ruft Entwurfseinheiten und allgemeine Metriken für die Schriftart ab. Diese Metriken gelten für alle Glyphen in einer Schriftart und werden von Anwendungen für Layoutberechnungen verwendet.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- GetGdiCompatibleMetrics-Methode Direct Write
- GetGdiCompatibleMetrics-Methode Direct Write , IDWriteFontFace-Schnittstelle
- IDWriteFontFace-Schnittstelle Direct Write , GetGdiCompatibleMetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290710"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>IDWriteFontFace::GetGdiCompatibleMetrics-Methode

Ruft Entwurfseinheiten und allgemeine Metriken für die Schriftart ab. Diese Metriken gelten für alle Glyphen in einer Schriftart und werden von Anwendungen für Layoutberechnungen verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*emSize* 
</dt> <dd>

Typ: **FLOAT**

Die logische Größe der Schriftart in DIP-Einheiten.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Typ: **FLOAT**

Die Anzahl der physischen Pixel pro DIP.

</dd> <dt>

*transformieren* \[ in, optional\]
</dt> <dd>

Typ: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Eine optionale Transformation, die auf die Glyphen und ihre Positionen angewendet wird. Diese Transformation wird nach der Skalierung angewendet, die durch den Schriftgrad und *pixelsPerDip* angegeben wird.

</dd> <dt>

*fontFaceMetrics* \[ out\]
</dt> <dd>

Typ: **[ **DWRITE-SCHRIFTARTMETRIKEN \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Ein Zeiger auf eine ZU füllende [**DWRITE \_ FONT \_ METRIC S-Struktur.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) Die von dieser Funktion zurückgegebenen Metriken befinden sich in Schriftentwurfseinheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Standard-HRESULT-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

