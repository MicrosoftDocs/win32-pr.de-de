---
title: BG_JOB_TYPE-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_TYPE-Enumeration definiert konstante Werte, die den Typ des Übertragungs Auftrags angeben, z. b. den Download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- BG_JOB_TYPE-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476173"
---
# <a name="bg_job_type-enumeration"></a>BG_JOB_TYPE-Enumeration

Die **BG_JOB_TYPE** -Enumeration definiert konstante Werte, die den Typ des Übertragungs Auftrags angeben, z. b. den Download.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

Gibt an, dass der Auftrag Dateien auf den Client herunterlädt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyjob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**Ibackgroundcopymanager:: kreatejob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





