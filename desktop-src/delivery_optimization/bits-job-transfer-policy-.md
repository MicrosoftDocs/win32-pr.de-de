---
title: BITS_JOB_TRANSFER_POLICY-Enumeration (deliveryoptimization. h)
description: Die BITS_JOB_TRANSFER_POLICY-Enumeration definiert ID-Werte, die den Do-Eigenschaften entsprechen.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- BITS_JOB_TRANSFER_POLICY-Enumeration
- BITS_JOB_TRANSFER_POLICY-Enumeration
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
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103243"
---
# <a name="bits_job_transfer_policy-enumeration"></a>BITS_JOB_TRANSFER_POLICY-Enumeration

Die **BITS_JOB_TRANSFER_POLICY** -Enumeration definiert ID-Werte, die den Do-Eigenschaften entsprechen.

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

Gibt an, dass der Auftrag übertragen wird, wenn die Konnektivität unabhängig von den Kosten verfügbar ist.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**
</dt> <dd>

Gibt an, dass der Auftrag übertragen wird, wenn eine Verbindung verfügbar ist, es sei denn, die Konnektivität unterliegt roamingzuschläge.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die keinem Zuschlag unterliegt.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die weder einem Aufpreis noch der beinahe-Erschöpfung unterliegt.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Gibt an, dass der Auftrag nur übertragen wird, wenn eine Konnektivität verfügbar ist, die keine Kosten oder Datenverkehrs Limits vorsieht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





