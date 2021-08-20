---
title: CHANGE_LOG_HEADER-Struktur
description: Der Änderungsprotokollheader.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER Struktur der Systemwiederherstellung
- PCHANGE_LOG_HEADER Strukturzeiger Systemwiederherstellung
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fbfc77aa0d737e43f1174edca2367aeb3b0bfb455b7b70c3de5a24d90214fb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047580"
---
# <a name="change_log_header-structure"></a>CHANGE \_ LOG \_ HEADER-Struktur

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

Der Änderungsprotokollheader.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**RecordHeader**
</dt> <dd>

Eine [**RECORD \_ HEADER-Struktur.**](record-header.md) Der **dwRecordType-Member** sollte auf RecordTypeLogHeader (0) festgelegt werden. Das **dwRecordSize-Element** sollte alle Elemente sowie den zusätzlichen **DWORD-Wert** berücksichtigen, der diesem Header folgt. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Dieser Member sollte auf 0xabcdef12 festgelegt werden.

</dd> <dt>

**dwLogVersion**
</dt> <dd>

Dieser Member sollte auf 2 festgelegt werden.

</dd> <dt>

**DataHeader**
</dt> <dd>

Eine [**RECORD \_ HEADER-Struktur.**](record-header.md) Der **dwRecordType-Member** sollte auf **RecordTypeVolumePath** (2) festgelegt werden.

</dd> <dt>

**byteData**
</dt> <dd>

Der Anfang einer auf NULL endenden Zeichenfolge, die den Volumepfad angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diesen Header folgt ein **DWORD-Wert,** der mit dem Wert des **dwRecordSize-Members** von **RecordHeader** identisch sein sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                            |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                       |



 

 





