---
description: 'IWICBitmapFlipRotator_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091158"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a>IWICBitmapFlipRotator-Funktion \_ "Proxy initialisieren" \_

Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***

Zeiger auf dieses [**IWICBitmapFlipRotator-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)

</dd> <dt>

*pISource* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die Eingabebitmapquelle.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**

Die [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) zum Spiegeln oder Drehen des Bilds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




