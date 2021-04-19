---
description: Proxy Funktion für die Methode "samatedecoderfromfilename".
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
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359584"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>IWICImagingFactory | \_ atedecoderfromfilename- \_ Proxy Funktion

Proxy Funktion für die Methode " [**samatedecoderfromfilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) ".

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

*pfactory* \[ in\]
</dt> <dd>

Typ: **IWICImagingFactory \** _

</dd> <dt>

_wzFilename * \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen eines zu erstellenden oder zu öffnenden Objekts angibt.

</dd> <dt>

*pguidVendor* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Die Anbieter-GUID für den Decoder.

</dd> <dt>

_dwDesiredAccess * \[ in\]
</dt> <dd>

Typ: **DWORD**

Der Zugriff auf das-Objekt, das gelesen oder geschrieben werden kann, oder beides.

Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte \[ Dateien \] ](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*metadataOptions* \[ in\]
</dt> <dd>

Typ: **[ **wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

Die [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) , die beim Erstellen des Decoders verwendet werden sollen.

</dd> <dt>

*ppidecoder* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Ein Zeiger, der einen Zeiger auf den neuen [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)empfängt.

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



 

