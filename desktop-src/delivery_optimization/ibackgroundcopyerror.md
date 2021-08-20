---
title: IBackgroundCopyError-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie die IBackgroundCopyError-Schnittstelle, um die Ursache eines Fehlers zu ermitteln und zu ermitteln, ob der Übertragungsprozess fortgesetzt werden kann.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- IBackgroundCopyError-Schnittstelle
- IBackgroundCopyError-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73e4dd3a74529bb95d1e80597579d6a0aa5885302b9b26d851dc341c9cd1a9a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101652"
---
# <a name="ibackgroundcopyerror-interface"></a>IBackgroundCopyError-Schnittstelle

Verwenden Sie **die IBackgroundCopyError-Schnittstelle,** um die Ursache eines Fehlers zu ermitteln und zu ermitteln, ob der Übertragungsprozess fortgesetzt werden kann.

DO erstellt nur dann ein Fehlerobjekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR. DO erstellt kein Fehlerobjekt, wenn eine **IBackgroundCopyXXXX-Schnittstellenmethode** fehlschlägt. Das Fehlerobjekt ist verfügbar, bis do mit der Übertragung von Daten (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING) für den Auftrag beginnt.

Um ein **IBackgroundCopyError-Objekt zu** erhalten, rufen Sie die [**IBackgroundCopyJob::GetError-Methode**](ibackgroundcopyjob-geterror.md) auf.

## <a name="members"></a>Member

Die **IBackgroundCopyError-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyError** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyError-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.<br/> |
| [**Getfile**](ibackgroundcopyerror-getfile-method.md)   | Ruft einen Schnittstellenzeiger auf das Dateiobjekt ab, das dem Fehler zugeordnet ist.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19C613A0-FCB8-4F28-81AE-897C3D078F81 definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

