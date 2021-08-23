---
description: Proxyfunktion für die InitializeCustom-Methode.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b68917782d768f526a21b16f22766c1a9add61eb5ee1987d27965b6f70a388db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088192"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a>IWICPalette \_ InitializeCustom \_ Proxy-Funktion

Proxyfunktion für die [**InitializeCustom-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Zeiger auf dieses [**IWICPalette-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pColors* \[ In\]
</dt> <dd>

Typ: **WICColor \***

Zeiger auf das Farbarray.

</dd> <dt>

*colorCount* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Anzahl der Farben in *pColors*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




