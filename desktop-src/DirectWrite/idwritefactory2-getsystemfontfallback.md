---
title: IDWriteFactory2 GetSystemFontFallback-Methode
description: Erstellt ein Fallbackobjekt für Schriftarten aus der Fallbackliste der Systemschriftart.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- GetSystemFontFallback-Methode – Direkter Schreibzugriff
- GetSystemFontFallback-Methode Direct Write, IDWriteFactory2-Schnittstelle
- IDWriteFactory2-Schnittstelle Direct Write , GetSystemFontFallback-Methode
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329445"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>IDWriteFactory2::GetSystemFontFallback-Methode

Erstellt ein Fallbackobjekt für Schriftarten aus der Fallbackliste der Systemschriftart.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fontFallback* \[ out\]
</dt> <dd>

Typ: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Enthält eine Adresse eines Zeigers auf das neu erstellte Schriftartfallbackobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 