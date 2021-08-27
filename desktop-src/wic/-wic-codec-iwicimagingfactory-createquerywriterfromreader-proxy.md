---
description: Proxyfunktion für die CreateQueryWriterFromReader-Methode.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6e03da055b5e48e21c044ce1708a8a8871c30fabeb860e486cde398650c23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711454"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a>Proxyfunktion "IWICImagingFactory \_ CreateQueryWriterFromReader" \_

Proxyfunktion für die [**CreateQueryWriterFromReader-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
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

*pIQueryReader* \[ In\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Der Metadatenabfrageleser, aus dem der Metadatenwriter erstellt werden soll.

</dd> <dt>

*pguidVendor* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Die Hersteller-GUID für den Metadatenabfrage-Writer.

</dd> <dt>

*ppIQueryWriter* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Ein Zeiger, der einen Zeiger auf einen neuen [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




