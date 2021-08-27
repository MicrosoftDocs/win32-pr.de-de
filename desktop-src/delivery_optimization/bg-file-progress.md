---
title: BG_FILE_PROGRESS -Struktur (Deliveryoptimization.h)
description: Die BG_FILE_PROGRESS-Struktur stellt dateibezogene Statusinformationen wie die Anzahl der übertragenen Bytes zur Verfügung.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS-Struktur
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd0bec0f21fb652ccc5c8d543f04816468fff9bc28db74a68a1d05c072a895a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047248"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS-Struktur

Die **BG_FILE_PROGRESS-Struktur** enthält dateibezogene Statusinformationen, z. B. die Anzahl der übertragenen Bytes.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**BytesTotal**
</dt> <dd>

Die Länge der Datei in Bytes. Wenn DO die Größe der Datei nicht bestimmen kann (z. B. wenn die Datei oder der Server nicht vorhanden ist), wird der Wert DO_UNKNOWN_FILE_SIZE.

Wenn Sie Bereiche aus einer Datei herunterladen, spiegelt **BytesTotal** die Gesamtzahl der Bytes wider, die Sie aus der Datei herunterladen möchten.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Anzahl der übertragenen Bytes.

</dd> <dt>

**Abgeschlossen**
</dt> <dd>

Bei Downloads ist der Wert **TRUE,** wenn die Datei für den Benutzer verfügbar ist. andernfalls ist der Wert **FALSE.** Dateien stehen dem Benutzer nach dem Aufruf der [**IBackgroundCopyJob::Complete-Methode zur**](ibackgroundcopyjob-complete.md) Verfügung. Wenn die **Complete-Methode** einen vorübergehenden Fehler generiert, sind die Dateien, die vor dem Fehler verarbeitet wurden, für den Benutzer verfügbar. die anderen nicht. Verwenden Sie **das Completed-Mitglied,** um zu bestimmen, ob die Datei für den Benutzer verfügbar ist, wenn Complete **fehlschlägt.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um zu ermitteln, ob DO die Datei übertragen hat, haben Sie die folgenden Folgenden:

-   Vergleichen **Sie BytesTransferred** mit **BytesTotal.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





