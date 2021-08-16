---
description: Proxyfunktion für die SetMetadataByName-Methode.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5ec3d018856b087762de70d6e2aea3e1f473db96b7ad989a62b3dfc2b5d3e691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206385"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a>Proxyfunktion \_ "SetMetadataByName" von IWICMetadataQueryWriter \_

Proxyfunktion für die [**SetMetadataByName-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\***

Zeiger auf dieses [**IWICMetadataQueryWriter-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)

</dd> <dt>

*wzName* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Der Name des Metadatenelements.

</dd> <dt>

*pvarValue* \[ In\]
</dt> <dd>

Typ: **const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \***

Die festzulegende Metadaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

