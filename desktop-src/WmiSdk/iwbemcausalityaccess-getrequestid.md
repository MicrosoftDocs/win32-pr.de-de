---
description: Die getRequestID-Methode gibt einen GUID-Wert (Global Unique Identifier) für eine Anforderung zurück. Eine GUID ist eine eindeutige 128-Bit-Zahl.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Iwbemkausalityaccess:: getRequestID-Methode (wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347701"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a>Iwbemkausalityaccess:: getRequestID-Methode

Die **getRequestID-** Methode gibt einen GUID-Wert (Global Unique Identifier) für eine Anforderung zurück. Eine GUID ist eine eindeutige 128-Bit-Zahl.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ vorgenommen\]
</dt> <dd>

Der GUID-Wert, der eine Anforderung eindeutig identifiziert. Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwbemkausalityaccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




