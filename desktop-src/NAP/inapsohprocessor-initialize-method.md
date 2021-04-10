---
title: Inapsohprocessor Initialize-Methode (napprotocol. h)
description: Initialisiert das Protokoll Paket und das SoH-Prozessor System. Diese Methode muss genau einmal aufgerufen werden.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode, NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956468"
---
# <a name="inapsohprocessorinitialize-method"></a>Inapsohprocessor:: Initialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **inapsohprocessor:: Initialize** -Methode werden das Protokoll Paket und das SoH-Prozessor System initialisiert. Diese Methode muss genau einmal aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SoH* \[ in\]
</dt> <dd>

Ein Zeiger auf das zu verarbeitende [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.

</dd> <dt>

*isrequest* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und **false** ist, wenn es sich um eine **sohresponse** handelt.

</dd> <dt>

*ID* \[ out\]
</dt> <dd>

Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA oder SHV enthält, der das Paket erstellt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>        | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>         | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt> </dl> | Das SoH-Paket ist ungültig.<br/>                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsohprocessor**](inapsohprocessor.md)
</dt> </dl>

 

 





