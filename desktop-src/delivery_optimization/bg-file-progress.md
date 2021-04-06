---
title: BG_FILE_PROGRESS-Struktur (deliveryoptimization. h)
description: Die BG_FILE_PROGRESS-Struktur liefert Datei bezogene Statusinformationen, wie z. b. die Anzahl der übertragenen Bytes.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS Struktur
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
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742865"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS Struktur

Die **BG_FILE_PROGRESS** -Struktur liefert Datei bezogene Statusinformationen, wie z. b. die Anzahl der übertragenen Bytes.

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

Die Länge der Datei in Bytes. Wenn die Größe der Datei nicht ermitteln kann (z. b. wenn die Datei oder der Server nicht vorhanden ist), wird der Wert DO_UNKNOWN_FILE_SIZE.

Wenn Sie Bereiche aus einer Datei herunterladen, spiegelt **bytesTotal** die Gesamtzahl der Bytes wider, die Sie aus der Datei herunterladen möchten.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Anzahl der übertragenen Bytes.

</dd> <dt>

**Abgeschlossen**
</dt> <dd>

Für Downloads ist der Wert **true** , wenn die Datei für den Benutzer verfügbar ist. Andernfalls ist der Wert **false**. Dateien sind nach dem Aufrufen der [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode für den Benutzer verfügbar. Wenn die **Complete** -Methode einen vorübergehenden Fehler generiert, sind die Dateien, die vor dem Auftreten des Fehlers verarbeitet wurden, für den Benutzer verfügbar. bei anderen handelt es sich nicht um. Verwenden Sie den **abgeschlossenen** Member, um zu ermitteln, ob die Datei für den Benutzer verfügbar ist, wenn der Vorgang **abgeschlossen** ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um festzustellen, ob die Datei übertragen wird, haben Sie folgende Möglichkeiten:

-   Vergleichen Sie **bytesTransferred** mit **bytesTotal**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**Ibackgroundcopyfile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





