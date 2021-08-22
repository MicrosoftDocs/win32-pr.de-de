---
title: IBackgroundCopyJob GetId-Methode (Deliveryoptimization.h)
description: Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId-Methode
- GetId-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetId-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01c696985b4b632223318675fd63f842b85ed6e27297ff1befebbac1b3fa9bce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755500"
---
# <a name="ibackgroundcopyjobgetid-method"></a>IBackgroundCopyJob::GetId-Methode

Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJobID* \[ out\]
</dt> <dd>

GUID, die den Auftrag innerhalb der DO-Warteschlange identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der COM **HRESULT-Standardwerte** bei Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Der Dienst generiert den Bezeichner beim [Erstellen](ibackgroundcopymanager-createjob.md) des Auftrags. Um den Bezeichner zum Abrufen eines [**IBackgroundCopyJob-Schnittstellenzeigers**](ibackgroundcopyjob-.md) für den Auftrag zu verwenden, rufen Sie die [**IBackgroundCopyManager::GetJob-Methode**](ibackgroundcopymanager-getjob.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





