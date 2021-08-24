---
description: Proxyfunktion für die CreateDecoderFromFilename-Methode.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dabc24d17fdac881537d45e47a8cc6808a1cf805ac14025d7fdfcfa50eea8500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056630"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>Proxyfunktion "IWICImagingFactory \_ CreateDecoderFromFilename" \_

Proxyfunktion für die [**CreateDecoderFromFilename-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFactory* \[ In\]
</dt> <dd>

Typ: **IWICImagingFactory \***

</dd> <dt>

*wzFilename* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen eines zu erstellenden oder zu öffnenden Objekts angibt.

</dd> <dt>

*pguidVendor* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Die Hersteller-GUID für den Decoder.

</dd> <dt>

*dwDesiredAccess* \[ In\]
</dt> <dd>

Typ: **DWORD**

Der Zugriff auf das -Objekt, das gelesen, geschrieben oder beides sein kann.

Weitere Informationen finden Sie unter [Dateisicherheits- und \[ Zugriffsberechtigungsdateien. \] ](../fileio/file-security-and-access-rights.md)

</dd> <dt>

*metadataOptions* \[ In\]
</dt> <dd>

Typ: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

Die [**WICDecodeOptions,**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) die beim Erstellen des Decoders verwendet werden sollen.

</dd> <dt>

*ppIDecoder* \[ out\]
</dt> <dd>

Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Ein Zeiger, der einen Zeiger auf den neuen [**IWICBitmapDecoder empfängt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

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



 

