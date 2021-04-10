---
title: IBackgroundCopyManager CreateJob-Methode (Deliveryoptimization.h)
description: Erstellt einen Auftrag.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Methode "kreatejob"
- Methode "kreatejob", ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, Methode "kreatejob"
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "104050641"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Ibackgroundcopymanager:: kreatejob-Methode

Erstellt einen Auftrag.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdisplayname* \[ in\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die einen anzeigen Amen für den Auftrag enthält. In der Regel wird der Anzeige Name verwendet, um den Auftrag auf einer Benutzeroberfläche zu identifizieren. Beachten Sie, dass mehr als ein Auftrag denselben anzeigen Amen aufweisen kann. Darf nicht **null** sein. Der Name ist auf 256 Zeichen beschränkt, ohne das NULL-Terminator.

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Typ des Übertragungs Auftrags, z. b. BG_JOB_TYPE_DOWNLOAD. Eine Liste der Übertragungs Typen finden Sie in der [**BG_JOB_TYPE**](bg-job-type.md) -Enumeration.

</dd> <dt>

*pjobid* \[ vorgenommen\]
</dt> <dd>

Identifiziert den Auftrag in der Warteschlange eindeutig. Verwenden Sie diesen Bezeichner, wenn Sie die [**ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md) -Methode aufrufen, um einen Auftrag aus der Warteschlange abzurufen.

</dd> <dt>

*ppjob* \[ vorgenommen\]
</dt> <dd>

Ein [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeiger, mit dem Sie die Eigenschaften des Auftrags ändern und die zu übertragenden Dateien angeben. Um den Auftrag in der Warteschlange zu aktivieren, müssen Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode abrufen. Release *ppjob* , wenn dies abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Der neue Auftrag wurde erfolgreich generiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann [dem Auftrag Dateien hinzufügen](https://www.bing.com/search?q=add+files+to+the+job) und [die Eigenschaften des Auftrags ändern](https://www.bing.com/search?q=change+the+job's+properties).

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

[**Ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
