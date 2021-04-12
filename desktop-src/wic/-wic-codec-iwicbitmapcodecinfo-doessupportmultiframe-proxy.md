---
description: Proxy Funktion für die doessupportmultiframe-Methode.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128965"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a>Iwicbitmapcodecinfo \_ doessupportmultiframe- \_ Proxy Funktion

Proxy Funktion für die [**doessupportmultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Zeiger auf dieses [_ *iwicbitmapcodecinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.

</dd> <dt>

*pfsupportmultiframe* \[ vorgenommen\]
</dt> <dd>

Typ: **bool \** _

Ein Zeiger, der _ *true** empfängt, wenn der Codec Multiframe-Bilder unterstützt. andernfalls **false**.

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



 

 




