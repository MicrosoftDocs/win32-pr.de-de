---
title: Ibackgroundcopymanager GetJob-Methode (deliveryoptimization. h)
description: Ruft einen angegebenen Auftrag aus der Übertragungs Warteschlange ab. In der Regel speichert Ihre Anwendung die Auftrags Kennung, sodass Sie den Auftrag später aus der Warteschlange abrufen können.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- GetJob-Methode
- GetJob-Methode, ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, GetJob-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342017"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>Ibackgroundcopymanager:: GetJob-Methode

Ruft einen angegebenen Auftrag aus der Übertragungs Warteschlange ab. In der Regel speichert Ihre Anwendung die Auftrags Kennung, sodass Sie den Auftrag später aus der Warteschlange abrufen können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*JobID* \[ in\]
</dt> <dd>

Identifiziert den Auftrag, der aus der Übertragungs Warteschlange abgerufen wird. Die Methode " [**kreatejob**](ibackgroundcopymanager-createjob.md) " gibt den Auftrags Bezeichner zurück.

</dd> <dt>

*ppjob* \[ vorgenommen\]
</dt> <dd>

Ein [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeiger auf den von *JobID* angegebenen Auftrag. Wenn Sie den Vorgang abgeschlossen haben, geben Sie *ppjob* frei

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                      | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | Der Auftrag wurde erfolgreich aus der Übertragungs Warteschlange abgerufen.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | Der Auftrag wurde nicht in der Warteschlange gefunden.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | Der Benutzer verfügt nicht über die Berechtigung zum Abrufen des Auftrags.<br/>      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager ist als 5ce34c0d-0dc9-4c1f -897c-daa1b78cee7c definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopymanager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**Ibackgroundcopymanager:: kreatejob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





