---
description: Proxyfunktion für die CreateQueryWriterFromBlockWriter-Methode.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 44af8d96d39afff1eba582f9dea283a09acd69dbd4fc6dc95b3f568919621efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965259"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a>IWICComponentFactory \_ CreateQueryWriterFromBlockWriter-Proxyfunktion \_

Proxyfunktion für die [**CreateQueryWriterFromBlockWriter-Methode.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\***

Zeiger auf dieses [**IWICComponentFactory-Objekt.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)

</dd> <dt>

*pIBlockWriter* \[ In\]
</dt> <dd>

Typ: **[ **IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\***

</dd> <dt>

*ppIQueryWriter* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

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



 

 




