---
title: IBackgroundCopyCallback-Schnittstelle (Deliveryoptimization.h)
description: Implementieren Sie die IBackgroundCopyCallback-Schnittstelle, um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder einen Fehler auft. Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags ab umfragen.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- IBackgroundCopyCallback-Schnittstelle
- IBackgroundCopyCallback-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165a1edcdb6bd70de8fad379fcc89d5afc36776348fd7751277614229a23377e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953640"
---
# <a name="ibackgroundcopycallback-interface"></a>IBackgroundCopyCallback-Schnittstelle

Implementieren Sie **die IBackgroundCopyCallback-Schnittstelle,** um eine Benachrichtigung zu erhalten, dass ein Auftrag abgeschlossen ist, geändert wurde oder einen Fehler auft. Clients verwenden diese Schnittstelle, anstatt den Status des Auftrags ab umfragen.

## <a name="members"></a>Member

Die **IBackgroundCopyCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyCallback** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Wird aufgerufen, wenn ein Fehler auftritt.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Wird aufgerufen, wenn ein Auftrag geändert wird.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Wird aufgerufen, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie zum Empfangen von Benachrichtigungen die [**IBackgroundCopyJob::SetNotifyInterface-Methode**](ibackgroundcopyjob-setnotifyinterface.md) auf, um den Schnittstellenzeiger auf Ihre **IBackgroundCopyCallback-Implementierung** anzugeben. Um anzugeben, welche Benachrichtigungen Sie empfangen möchten, rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](ibackgroundcopyjob-setnotifyflags.md) auf.

DO rufen Ihre Rückrufe auf, solange der Schnittstellenzeiger gültig ist. Die Benachrichtigungsschnittstelle ist nicht mehr gültig, wenn Ihre Anwendung beendet wird. DIE Benachrichtigungsschnittstelle wird nicht beibehalten. Daher sollte der Initialisierungsprozess Ihrer Anwendung die [**SetNotifyInterface-Methode**](ibackgroundcopyjob-setnotifyinterface.md) für die vorhandenen Aufträge aufrufen, für die Sie eine Benachrichtigung erhalten möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

