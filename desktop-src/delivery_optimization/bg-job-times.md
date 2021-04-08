---
title: BG_JOB_TIMES-Struktur (deliveryoptimization. h)
description: Die BG_JOB_TIMES-Struktur stellt auftragsbezogene Zeitstempel bereit.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- BG_JOB_TIMES Struktur
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740321"
---
# <a name="bg_job_times-structure"></a>BG_JOB_TIMES Struktur

Die **BG_JOB_TIMES** -Struktur stellt auftragsbezogene Zeitstempel bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Member

<dl> <dt>

**CreationTime**
</dt> <dd>

Zeitpunkt, zu dem der Auftrag erstellt wurde. Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.

</dd> <dt>

**ModificationTime**
</dt> <dd>

Uhrzeit, zu der der Auftrag zuletzt geändert wurde oder die Bytes übertragen wurden. Durch das Hinzufügen von Dateien oder das Aufrufen einer der Set-Methoden in den [ * *ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) -Schnittstellen wird dieser Wert geändert. Außerdem wird dieser Wert durch Änderungen am Status des Auftrags und durch Aufrufen der Methoden [_ *Suspend* *](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)und [**Complete**](ibackgroundcopyjob-complete.md) geändert. Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.

</dd> <dt>

**Transfercompletiontime**
</dt> <dd>

Zeitpunkt, zu dem der Auftrag in den BG_JOB_STATE_TRANSFERRED Status eingetreten ist Die Uhrzeit wird als [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)angegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyjob:: gettimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

