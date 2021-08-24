---
title: IBackgroundCopyJob SetNotifyInterface-Methode (Deliveryoptimization.h)
description: Identifiziert Ihre Implementierung der IBackgroundCopyCallback-Schnittstelle für do. Verwenden Sie die IBackgroundCopyCallback-Schnittstelle, um Benachrichtigungen über auftragsbezogene Ereignisse zu erhalten.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- SetNotifyInterface-Methode
- SetNotifyInterface-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, SetNotifyInterface-Methode
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
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793409"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>IBackgroundCopyJob::SetNotifyInterface-Methode

Identifiziert Ihre Implementierung der [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) für do. Verwenden Sie die **IBackgroundCopyCallback-Schnittstelle,** um Benachrichtigungen über auftragsbezogene Ereignisse zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

Ein [**IBackgroundCopyCallback-Schnittstellenzeiger.**](ibackgroundcopycallback.md) Um den aktuellen Rückrufschnittstellenzeiger zu entfernen, legen Sie diesen Parameter auf **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                              | Beschreibung                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl> | Der Benachrichtigungsschnittstellenzeiger wurde erfolgreich festgelegt.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nur auf, wenn Sie die [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) implementieren. Verwenden Sie **die SetNotifyInterface-Methode** in Verbindung mit der [**SetNotifyFlags-Methode,**](ibackgroundcopyjob-setnotifyflags.md) um den Typ der Benachrichtigung anzugeben, die Sie empfangen möchten.

Die Benachrichtigungsschnittstelle wird ungültig, wenn Ihre Anwendung beendet wird. DIE Benachrichtigungsschnittstelle wird nicht beibehalten. Daher sollte der Initialisierungsprozess Ihrer Anwendung die **SetNotifyInterface-Methode** für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten. Wenn Sie Zustands- und Fortschrittsinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, sollten Sie während der Anwendungsin initialisierung Status- und Statusinformationen erhalten.

Nur der Besitzer/Ersteller des Auftrags oder ein Administrator kann sich für Benachrichtigungen registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





