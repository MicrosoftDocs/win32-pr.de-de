---
title: IDWriteFactory2 getsystemfontfallback-Methode
description: Erstellt ein Schriftart Fall Back Objekt aus der System Schriftart-fallbackliste.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Getsystemfontfallback-Methode direkt schreiben
- Getsystemfontfallback-Methode Direct Write, IDWriteFactory2-Schnittstelle
- IDWriteFactory2 Interface Direct Write, getsystemfontfallback-Methode
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390764"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>IDWriteFactory2:: getsystemfontfallback-Methode

Erstellt ein Schriftart Fall Back Objekt aus der System Schriftart-fallbackliste.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fontfallback* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **idschreitefontfallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Enthält eine Adresse eines Zeigers auf das neu erstellte Schriftart Fall Back Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 