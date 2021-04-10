---
title: BITS_JOB_PROPERTY_VALUE-Struktur (deliveryoptimization. h)
description: Die BITS_JOB_PROPERTY_VALUE Union stellt den Eigenschafts Wert des Do-Auftrags basierend auf dem Wert der BITS_JOB_PROPERTY_ID-Enumeration bereit.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE Struktur
- BITS_JOB_PROPERTY_VALUE Struktur
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103664"
---
# <a name="bits_job_property_value-structure"></a>BITS_JOB_PROPERTY_VALUE Struktur

Die **BITS_JOB_PROPERTY_VALUE** Union stellt den Eigenschafts Wert des Do-Auftrags basierend auf dem Wert der [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) -Enumeration bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**DWORD**
</dt> <dd>

Dieser Wert wird zurückgegeben, wenn die Enumeration-Eigenschaften-ID verwendet wird **BITS_JOB_PROPERTY_ID_COST_FLAGS** und wird als [Übertragungs Richtlinie](https://www.bing.com/search?q=transfer+policy) für den Do-Auftrag angewendet.

</dd> <dt>

**CLSID**
</dt> <dd>

Dieser Wert wird zurückgegeben, wenn die enumerationseigenschafts-ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** verwendet wird, und stellt die CLSID des Rückruf Objekts dar, das bei der do-Aufgabe registriert werden soll

</dd> <dt>

**Aktivieren**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

**UInt64**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

**Target**
</dt> <dd>

Wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





