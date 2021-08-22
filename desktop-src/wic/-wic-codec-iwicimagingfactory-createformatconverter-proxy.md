---
description: Proxyfunktion für die CreateFormatConverter-Methode.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9d171847df9fb3b7fdcd15960d2caa91be09a65da2c8bb4d664aa714944435b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088292"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a>IWICImagingFactory \_ \_ CreateFormatConverter-Proxyfunktion

Proxyfunktion für die [**CreateFormatConverter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFactory* \[ In\]
</dt> <dd>

Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIFormatConverter* \[ out\]
</dt> <dd>

Typ: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***

Ein Zeiger, der einen Zeiger auf einen neuen [**IWICFormatConverter empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

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



 

 




