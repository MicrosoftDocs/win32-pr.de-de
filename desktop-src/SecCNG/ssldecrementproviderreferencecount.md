---
description: Dekrementierungen der Verweise auf den SSL-Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Ssldecrementproviderreferencecount-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959432"
---
# <a name="ssldecrementproviderreferencecount-function"></a>Ssldecrementproviderreferencecount-Funktion

Die **ssldecrementproviderreferencecount-Funktion dekrementierungen** die Verweise auf den SSL-Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                        | BESCHREIBUNG                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt> **\_ Ungültiger \_ handle**</dt> <dt>0xc0000008l</dt> </dl> | Das SSL-Anbieter Handle ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

