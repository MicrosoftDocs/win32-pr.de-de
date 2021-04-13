---
title: Ibackgroundcopyjob setnotifyinterface-Methode (deliveryoptimization. h)
description: Gibt die Implementierung der ibackgroundcopycallback-Schnittstelle an. Verwenden Sie die ibackgroundcopycallback-Schnittstelle zum Empfangen von Benachrichtigungen über auftragsbezogene Ereignisse.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Setnotifyinterface-Methode
- Setnotifyinterface-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnotifyinterface-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340618"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Ibackgroundcopyjob:: setnotifyinterface-Methode

Gibt die Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle an. Verwenden Sie die **ibackgroundcopycallback** -Schnittstelle zum Empfangen von Benachrichtigungen über auftragsbezogene Ereignisse.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnotifyinterface* 
</dt> <dd>

Ein [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstellen Zeiger. Legen Sie diesen Parameter auf **null** fest, um den aktuellen Rückruf Schnittstellen Zeiger zu entfernen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Der Benachrichtigungs Schnittstellen Zeiger wurde erfolgreich festgelegt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Methode nur auf, wenn Sie die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle implementieren. Verwenden Sie die **setnotifyinterface** -Methode in Verbindung mit der [**setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode, um den Typ der Benachrichtigung anzugeben, die Sie empfangen möchten.

Die Benachrichtigungs Schnittstelle wird ungültig, wenn die Anwendung beendet wird. Behält die Benachrichtigungs Schnittstelle nicht bei. Folglich sollte der Initialisierungs Prozess ihrer Anwendung die **setnotifyinterface** -Methode für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten. Wenn Sie Zustands-und Statusinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, rufen Sie während der Anwendungs Initialisierung Informationen zum Status und zum Fortschritt ab.

Nur der Auftrags Besitzer/-Ersteller oder ein Administrator kann sich für Benachrichtigungen registrieren.

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

[**Ibackgroundcopycallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Ibackgroundcopyjob:: getnotifyinterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





