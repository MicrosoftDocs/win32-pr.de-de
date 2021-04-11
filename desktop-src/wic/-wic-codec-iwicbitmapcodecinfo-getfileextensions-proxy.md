---
description: Proxy Funktion für die getFileExtensions-Methode.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343229"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a>Iwicbitmapcodecinfo \_ getFileExtensions- \_ Proxy Funktion

Proxy Funktion für die [**getFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Zeiger auf dieses [_ *iwicbitmapcodecinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.

</dd> <dt>

*cchfileextensions* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des Dateinamen-Erweiterungs Puffers.

</dd> <dt>

*wzfileextensions* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger, der die Dateinamen Erweiterungen empfängt, die dem Codec zugeordnet sind.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Typ: **uint \** _

Die tatsächliche Puffergröße, die benötigt wird, um alle dem Codec zugeordneten Dateinamen Erweiterungen abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




