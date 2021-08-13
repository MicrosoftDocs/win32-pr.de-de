---
title: BITS_JOB_TRANSFER_POLICY -Enumeration (Deliveryoptimization.h)
description: Die BITS_JOB_TRANSFER_POLICY-Enumeration definiert ID-Werte, die DO-Eigenschaften entspricht.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- BITS_JOB_TRANSFER_POLICY Enumeration
- BITS_JOB_TRANSFER_POLICY Enumeration
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 022d12b78416ce4ec84cf02ae8696f17bf5c315a207ae04f28a8980f6aaac073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544598"
---
# <a name="bits_job_transfer_policy-enumeration"></a>BITS_JOB_TRANSFER_POLICY Enumeration

Die **BITS_JOB_TRANSFER_POLICY-Enumeration** definiert ID-Werte, die DO-Eigenschaften entspricht.

## <a name="syntax"></a>Syntax


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**
</dt> <dd>

Gibt an, dass der Auftrag übertragen wird, wenn die Konnektivität verfügbar ist, unabhängig von den Kosten.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**
</dt> <dd>

Gibt an, dass der Auftrag übertragen wird, wenn die Konnektivität verfügbar ist, es sei denn, diese Konnektivität unterliegt Roaminggebühren.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Verbindung verfügbar ist, die keinen Zuschlägen unterliegt.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Verbindung verfügbar ist, die weder einem Zuschlag noch einer nahezuen Erschöpfung unterliegt.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Verbindung verfügbar ist, die keine Kosten oder Grenzwerte für den Datenverkehr verursacht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



 

 





