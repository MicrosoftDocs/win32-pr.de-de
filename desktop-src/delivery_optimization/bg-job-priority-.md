---
title: BG_JOB_PRIORITY-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_PRIORITY-Enumeration definiert die Konstanten Werte, die die Prioritätsstufe eines Auftrags angeben.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY-Enumeration
- BG_JOB_PRIORITY-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040473"
---
# <a name="bg_job_priority-enumeration"></a>BG_JOB_PRIORITY-Enumeration

Die **BG_JOB_PRIORITY** -Enumeration definiert die Konstanten Werte, die die Prioritätsstufe eines Auftrags angeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Überträgt den Auftrag im Vordergrund. Vordergrund Übertragungen konkurrieren an der Netzwerkbandbreite mit anderen Anwendungen, die die Netzwerkleistung des Benutzers beeinträchtigen können. Dies ist die höchste Prioritätsstufe.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Überträgt den Auftrag im Hintergrund. Bei Hintergrund Übertragungen wird ein kleiner Prozentsatz der Netzwerkbandbreite verwendet.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Do-Verhalten ist für alle nicht-Vordergrund-Aufträge identisch. Ausführliche Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Do-Verhalten ist für alle nicht-Vordergrund-Aufträge identisch. Ausführliche Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mehrere Vordergrund-und Hintergrund Übertragungen können gleichzeitig stattfinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyjob:: GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Ibackgroundcopyjob:: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





