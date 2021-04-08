---
title: Inapsystemhealthvalidationrequest setprivatedata-Methode (napsystemhealthvalidator. h)
description: Ermöglicht dem napserver das Speichern von Zustandsinformationen.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Setprivatedata-Methode NAP
- Setprivatedata-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, setprivatedata-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742224"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a>Inapsystemhealthvalidationrequest:: setprivatedata-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthvalidationrequest:: setprivatedata** -Methode ermöglicht dem napserver das Speichern von Zustandsinformationen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PRIVATEDATA* \[ in\]
</dt> <dd>

Ein Zeiger auf ein [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) -datenblob, das die nicht transparenten Zustandsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Nur der napserver kann das datenblob interpretieren.

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

 

 





