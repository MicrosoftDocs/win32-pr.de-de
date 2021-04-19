---
title: Ibackgroundcopyjob GetId-Methode (deliveryoptimization. h)
description: Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId-Methode
- GetId-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetId-Methode
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
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339968"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Ibackgroundcopyjob:: GetId-Methode

Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pjobid* \[ vorgenommen\]
</dt> <dd>

GUID, die den Auftrag innerhalb der do-Warteschlange identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Der Dienst generiert den Bezeichner, wenn Sie den Auftrag [Erstellen](ibackgroundcopymanager-createjob.md) . Um den Bezeichner zum Abrufen eines [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeigers für den Auftrag zu verwenden, rufen Sie die [**ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md) -Methode auf.

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

[**Ibackgroundcopymanager:: kreatejob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**Ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





