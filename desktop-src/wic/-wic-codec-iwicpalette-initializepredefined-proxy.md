---
description: Proxy Funktion für die initializevordefinierten-Methode.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758850"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a>Iwicpalette \_ initializevordefinierten \_ Proxy Funktion

Proxy Funktion für die [**initializevordefinierten**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Zeiger auf dieses [_ *iwicpalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.

</dd> <dt>

*epalettetype* \[ in\]
</dt> <dd>

Typ: **[ **wicbitmappalettetype**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Der gewünschte vordefinierte Palettentyp.

</dd> <dt>

*faddtransparentcolor* \[ in\]
</dt> <dd>

Typ: **bool**

Die optionale übergeordnete Farbe, die der Palette hinzugefügt werden soll. Wenn keine transparente Farbe erforderlich ist, verwenden Sie 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




