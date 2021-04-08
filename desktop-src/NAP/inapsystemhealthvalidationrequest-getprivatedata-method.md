---
title: Inapsystemhealthvalidationrequest getprivatedata-Methode (napsystemhealthvalidator. h)
description: Ermöglicht dem napserver das Abrufen von Zustandsinformationen.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Getprivatedata-Methode NAP
- Getprivatedata-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getprivatedata-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743345"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a>Inapsystemhealthvalidationrequest:: getprivatedata-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthvalidationrequest:: getprivatedata** -Methode ermöglicht dem napserver das Abrufen von Zustandsinformationen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PRIVATEDATA* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen nicht transparenten Daten-BLOB mit [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , der Zustandsinformationen enthält.

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

 

 





