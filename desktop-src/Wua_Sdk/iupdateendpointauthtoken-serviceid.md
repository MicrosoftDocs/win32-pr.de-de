---
description: Ruft den Bezeichner des Diensts ab, der mit dem Endpunkt Token authentifiziert werden soll.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Iupdateendpointauthtoken:: serviceid-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359863"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>Iupdateendpointauthtoken:: serviceid-Methode

Ruft den Bezeichner des Diensts ab, der mit dem Endpunkt Token authentifiziert werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pserviceid* \[ vorgenommen\]
</dt> <dd>

Der Bezeichner des Dienstanbieter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iupdateendpointauthtoken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




