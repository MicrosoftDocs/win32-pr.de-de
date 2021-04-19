---
title: Idwrite-fontface getgdicompatiblemetrics-Methode
description: Ruft Entwurfs Einheiten und allgemeine Metriken für die Schriftart ab. Diese Metriken gelten für alle Symbole innerhalb eines fontface und werden von Anwendungen für Layoutberechnungen verwendet.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Getgdicompatiblemetrics-Methode direkt schreiben
- Getgdicompatiblemetrics-Methode direkt schreiben, idschreitefontface-Schnittstelle
- Idwrite Test fontface Interface Direct Write, getgdicompatiblemetrics-Methode
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
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370001"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Idschreitefontface:: getgdicompatiblemetrics-Methode

Ruft Entwurfs Einheiten und allgemeine Metriken für die Schriftart ab. Diese Metriken gelten für alle Symbole innerhalb eines fontface und werden von Anwendungen für Layoutberechnungen verwendet.

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

Typ: **float**

Die logische Größe der Schriftart in DIP-Einheiten.

</dd> <dt>

*Pixel sperdip* 
</dt> <dd>

Typ: **float**

Die Anzahl der physischen Pixel pro DIP.

</dd> <dt>

*Transformation* \[ in, optional\]
</dt> <dd>

Typ: Konstante **[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Eine optionale Transformation, die auf die Symbole und deren Positionen angewendet wird. Diese Transformation wird nach der durch Schriftart Größe und *pixelsperdip* angegebenen Skalierung angewendet.

</dd> <dt>

*fontfacemetrics* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **dwrite- \_ Schriftart \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Ein Zeiger auf eine [**dwrite- \_ Schriftart \_ Metrik**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S-Struktur, die ausgefüllt werden soll. Die von dieser Funktion zurückgegebenen Metriken sind in Schriftart Entwurfs Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Standard-HRESULT-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

