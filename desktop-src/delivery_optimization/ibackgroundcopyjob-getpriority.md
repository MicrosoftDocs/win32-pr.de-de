---
title: Ibackgroundcopyjob GetPriority-Methode (deliveryoptimization. h)
description: Ruft die Prioritätsstufe für den Auftrag ab. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- GetPriority-Methode
- GetPriority-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetPriority-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344473"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a>Ibackgroundcopyjob:: GetPriority-Methode

Ruft die Prioritätsstufe für den Auftrag ab. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppriority* \[ vorgenommen\]
</dt> <dd>

Die Priorität des Auftrags in Bezug auf andere Aufträge in der Übertragungs Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Die Prioritätsstufe wurde erfolgreich abgerufen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Ibackgroundcopyjob:: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





