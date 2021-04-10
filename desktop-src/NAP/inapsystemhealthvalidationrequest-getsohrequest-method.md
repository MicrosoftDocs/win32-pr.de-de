---
title: Inapsystemhealthvalidationrequest getsohrequest-Methode (napsystemhealthvalidator. h)
description: Ermöglicht System Integritätsprüfungen (SHVs) das Abrufen und Überprüfen der sohrequest-Informationen, die von Ihrem System Integritäts-Agent (System Health Agent, SHA) auf dem Client gesendet werden.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106418"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>Inapsystemhealthvalidationrequest:: getsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **inapsystemhealthvalidationrequest:: getsohrequest** -Methode können System Integritätsprüfungen (SHVs) die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Informationen abrufen und überprüfen, die von ihren Systemintegritäts-Agent-Entsprechungen (System Health Agent, SHA) auf dem Client gesendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohrequest* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Struktur.

</dd> <dt>

*napsystemgenerated* \[ vorgenommen\]
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn das SoH vom NAPAgent im Auftrag des SHA erstellt wurde, andernfalls **false** . Es wird hauptsächlich verwendet, um einen SHA-Fehler für den SHV anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der *sohrequest* -Parameter gibt möglicherweise **null** zurück, wenn der Client kein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) an den SHV gesendet hat. In diesem Szenario kann der SHV eine **sohresponse** mit dem Fehlercode " [**NAP \_ E \_ Missing \_ SoH**](nap-error-constants.md)" auffüllen.

Wenn der Parameter " *napsystemgenerated* " den Wert " **true**" hat, lautet das *sohrequest* -Format wie folgt:

-   [**sohattributetypesystemhealthid**](sohattributetype-enum.md)= <id>
-   [**sohattributetypefailurecategory**](sohattributetype-enum.md) =  [ **failurecategoryclientcomponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohattributetypeerrorcodes**](sohattributetype-enum.md)  =  [ **<SHA-Failure-Error-Code>**](nap-error-constants.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





