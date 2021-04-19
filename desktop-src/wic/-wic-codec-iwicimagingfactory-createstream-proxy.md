---
description: Proxy Funktion für die Methode "kreatestream".
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363345"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a>IWICImagingFactory- \_ Funktion "foratestream \_ Proxy"

Proxy Funktion für die Methode " [**kreatestream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) ".

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfactory* \[ in\]
</dt> <dd>

Typ: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIWICStream * \[ out\]
</dt> <dd>

Typ: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***

Ein Zeiger, der einen Zeiger auf einen neuen [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)empfängt.

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



 

 




