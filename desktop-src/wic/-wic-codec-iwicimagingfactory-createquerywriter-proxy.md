---
description: Proxyfunktion für die CreateQueryWriter-Methode.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: IWICImagingFactory_CreateQueryWriter_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe37af1ebcc4c8fd95b578d363fdb498cb06c22f354b7e2ef8f5ed7a3b29ac01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088272"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a>IWICImagingFactory \_ \_ CreateQueryWriter-Proxyfunktion

Proxyfunktion für die [**CreateQueryWriter-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFactory* \[ In\]
</dt> <dd>

Typ: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*guidMetadataFormat* \[ In\]
</dt> <dd>

Typ: **REFGUID**

Die GUID für das gewünschte Metadatenformat.

</dd> <dt>

*pguidVendor* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Die Hersteller-GUID des Metadatenwriters.

</dd> <dt>

*ppIQueryWriter* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Ein Zeiger, der einen Zeiger auf einen neuen [**IWICMetadataQueryWriter empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)

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



 

 




