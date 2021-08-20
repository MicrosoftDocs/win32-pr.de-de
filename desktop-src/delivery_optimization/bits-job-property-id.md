---
title: BITS_JOB_PROPERTY_ID-Enumeration (Deliveryoptimization.h)
description: Die BITS_JOB_PROPERTY_ID-Enumeration gibt die ID der Eigenschaft für den DO-Auftrag an. Diese Enumeration wird in der BITS_JOB_PROPERTY_VALUE Union verwendet, um den Typ des in der Union enthaltenen Werts zu bestimmen.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- BITS_JOB_PROPERTY_ID-Enumeration
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803e776bd635cd600bf664354dda8703d224dffcd63ea751919875a6ea69233d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047148"
---
# <a name="bits_job_property_id-enumeration"></a>BITS_JOB_PROPERTY_ID-Enumeration

Die **BITS_JOB_PROPERTY_ID-Enumeration** gibt die ID der Eigenschaft für den DO-Auftrag an. Diese Enumeration wird in der [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union verwendet, um den Typ des in der Union enthaltenen Werts zu bestimmen.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**
</dt> <dd>

Die ID, die zum [Steuern des Übertragungsverhaltens](https://www.bing.com/search?q=control+transfer+behavior) über Mobilfunknetze und/oder ähnliche Netzwerke verwendet wird. Diese Eigenschaft kann während einer Übertragung geändert werden, während die neuen Kostenflags sofort wirksam werden.

Diese Eigenschaft verwendet das **Dword-Feld** **BITS_JOB_PROPERTY_VALUE.**

</dd> <dt>

<span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**
</dt> <dd>

Die ID, die zum [Registrieren eines COM-Rückrufs](https://www.bing.com/search?q=register+a+COM+callback) durch CLSID verwendet wird, um Benachrichtigungen über den Fortschritt und den Abschluss eines DO-Auftrags zu erhalten. Die CLSID muss auf eine Klasse verweisen, die einem registrierten out-of-process COM-Server zugeordnet ist. Sie kann auch auf **GUID_NULL** festgelegt werden, um eine zuvor festgelegte Benachrichtigungs-CLSID zu löschen.

Diese Eigenschaft verwendet das **CLsID-Feld** **BITS_JOB_PROPERTY_VALUE.**

</dd> <dt>

<span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**
</dt> <dd>

Wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> <dt>

[**IBackgroundCopyJob5::SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[**IBackgroundCopyJob5::GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





