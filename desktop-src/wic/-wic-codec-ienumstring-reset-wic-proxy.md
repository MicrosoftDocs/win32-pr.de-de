---
description: 'Windows Imaging Component (WIC)-Proxy Funktion für IEnumString:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348985"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>IEnumString-zurück setzung der \_ \_ WIC- \_ Proxy Funktion

Windows Imaging Component (WIC)-Proxy Funktion für IEnumString:: Reset.

## <a name="syntax"></a>Syntax


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **IEnumString \** _

Paramde

</dd> <dt>

_celt * \[ in\]
</dt> <dd>

Typ: **ulong**

</dd> <dt>

*rgelt* \[ vorgenommen\]
</dt> <dd>

Typ: **lpolestr \** _

</dd> <dt>

_pceltFetched * \[ out\]
</dt> <dd>

Typ: **ulong \** _

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



 

 




