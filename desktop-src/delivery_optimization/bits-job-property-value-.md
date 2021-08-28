---
title: BITS_JOB_PROPERTY_VALUE -Struktur (Deliveryoptimization.h)
description: Die BITS_JOB_PROPERTY_VALUE Union stellt den Eigenschaftswert des DO-Auftrags basierend auf dem Wert der BITS_JOB_PROPERTY_ID dar.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE-Struktur
- BITS_JOB_PROPERTY_VALUE-Struktur
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
ms.openlocfilehash: 7f7366f993f23a16aa6c0d4486c33f45cd501962add9ab524a008aba51cd8ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755730"
---
# <a name="bits_job_property_value-structure"></a>BITS_JOB_PROPERTY_VALUE-Struktur

Die **BITS_JOB_PROPERTY_VALUE** Union stellt den Eigenschaftswert des DO-Auftrags basierend auf dem Wert der BITS_JOB_PROPERTY_ID [**dar.**](bits-job-property-id.md)

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

**Dword**
</dt> <dd>

Dieser Wert wird zurückgegeben, wenn die  enum-Eigenschaften-ID BITS_JOB_PROPERTY_ID_COST_FLAGS und als Übertragungsrichtlinie für [den](https://www.bing.com/search?q=transfer+policy) DO-Auftrag angewendet wird.

</dd> <dt>

**Clsid**
</dt> <dd>

Dieser Wert wird zurückgegeben, wenn die  enum-Eigenschaften-ID BITS_JOB_PROPERTY_NOTIFICATION_CLSID und stellt die CLSID des Rückrufobjekts dar, das beim DO-Auftrag registriert werden soll.

</dd> <dt>

**Aktivieren**
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

**Uint64**
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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





