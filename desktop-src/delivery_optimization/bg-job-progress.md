---
title: BG_JOB_PROGRESS-Struktur (deliveryoptimization. h)
description: Die BG_JOB_PROGRESS Struktur bietet auftragsbezogene Statusinformationen, wie z. b. die Anzahl von Bytes und übertragenen Dateien. Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- BG_JOB_PROGRESS Struktur
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518548"
---
# <a name="bg_job_progress-structure"></a>BG_JOB_PROGRESS Struktur

Die **BG_JOB_PROGRESS** Struktur bietet auftragsbezogene Statusinformationen, wie z. b. die Anzahl von Bytes und übertragenen Dateien. Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**BytesTotal**
</dt> <dd>

Gesamtanzahl der Bytes, die für alle Dateien im Auftrag übertragen werden sollen. Wenn der Wert BG_SIZE_UNKNOWN ist, wurde die Gesamtgröße aller Dateien im Auftrag nicht ermittelt. Dieser Wert wird nicht festgelegt, wenn nicht die Größe einer der Dateien bestimmt werden kann. Wenn z. b. die angegebene Datei bzw. der angegebene Server nicht vorhanden ist, kann die Größe der Datei von nicht bestimmt werden.

Wenn Sie Bereiche aus der Datei herunterladen, enthält **bytesTotal** die Gesamtzahl der Bytes, die Sie aus der Datei herunterladen möchten.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Anzahl der übertragenen Bytes.

</dd> <dt>

**Filestotal**
</dt> <dd>

Die Gesamtanzahl der Dateien, die für diesen Auftrag übertragen werden sollen.

</dd> <dt>

**Filestransferred**
</dt> <dd>

Anzahl der übertragenen Dateien.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Ibackgroundcopyjob:: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





