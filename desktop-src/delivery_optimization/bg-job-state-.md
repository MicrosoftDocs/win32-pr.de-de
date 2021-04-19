---
title: BG_JOB_STATE-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_STATE-Enumeration definiert konstante Werte für die verschiedenen Zustände eines Auftrags.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- BG_JOB_STATE-Enumeration
- BG_JOB_STATE-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339539"
---
# <a name="bg_job_state-enumeration"></a>BG_JOB_STATE-Enumeration

Die **BG_JOB_STATE** -Enumeration definiert konstante Werte für die verschiedenen Zustände eines Auftrags.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Gibt an, dass sich der Auftrag in der Warteschlange befindet und auf die Laufzeiten wartet. Wenn ein Benutzer sich abmeldet, während der Auftrag übertragen wird, wechselt der Auftrag in den Zustand "in Warteschlange".

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Gibt an, dass Daten für den Auftrag übertragen.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Gibt an, dass der Auftrag angehalten wurde (angehalten). Zum Aussetzen eines Auftrags wird die [**ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) -Methode aufgerufen. Der Auftrag bleibt angehalten, bis Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)-, [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)-Methode oder die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode aufgerufen haben.

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Gibt an, dass ein nicht BEHEB barer Fehler aufgetreten ist (der Dienst kann die Datei nicht übertragen). Wenn der Fehler, wie z. b. der Fehler "Zugriff verweigert", korrigiert werden kann, müssen Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aufrufen, nachdem der Fehler behoben wurde. Wenn der Fehler jedoch nicht korrigiert werden kann, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf, um den Auftrag abzubrechen, oder rufen Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode auf, um den Teil eines Download Auftrags zu akzeptieren, der erfolgreich übertragen wurde.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Gibt an, dass ein BEHEB barer Fehler aufgetreten ist. Führt einen Wiederholungsversuch für Aufträge im vorübergehenden Fehlerstatus basierend auf der internen Wiederholungs Konfiguration aus. Der Status des Auftrags ändert sich in **BG_JOB_STATE_ERROR** , wenn der Auftrag nicht fortgesetzt werden kann (siehe [**ibackgroundcopyjob:: setnoprogresstimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Gibt an, dass der Auftrag erfolgreich verarbeitet wurde. Sie müssen die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode anrufen, um den Abschluss des Auftrags zu bestätigen und die Dateien für den Client verfügbar zu machen.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Gibt an, dass Sie die Methode [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) aufgerufen haben, um zu bestätigen, dass der Auftrag erfolgreich abgeschlossen wurde.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Gibt an, dass Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode aufgerufen haben, um den Auftrag abzubrechen (entfernen Sie den Auftrag aus der Übertragungs Warteschlange).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





