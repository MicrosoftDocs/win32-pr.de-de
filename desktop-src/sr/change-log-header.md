---
title: CHANGE_LOG_HEADER Struktur
description: Der Änderungsprotokoll Header.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER Struktur System Wiederherstellung
- PCHANGE_LOG_HEADER Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391580"
---
# <a name="change_log_header-structure"></a>\_Struktur der Protokoll \_ Kopfzeile ändern

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

Der Änderungsprotokoll Header.

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

**Recordheader**
</dt> <dd>

Eine [**Daten Satz \_ Header**](record-header.md) -Struktur. Der **dwrecordtype** -Member sollte auf recordtypelogheader (0) festgelegt werden. Das **dwrecordsize** -Element muss alle Member sowie den zusätzlichen **DWORD** -Wert berücksichtigen, der diesem Header folgt. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**dwmagicnum**
</dt> <dd>

Dieser Member sollte auf 0xabcdef12 festgelegt werden.

</dd> <dt>

**dwlogversion**
</dt> <dd>

Dieser Member sollte auf 2 festgelegt werden.

</dd> <dt>

**Dataheader**
</dt> <dd>

Eine [**Daten Satz \_ Header**](record-header.md) -Struktur. Der **dwrecordtype** -Member sollte auf **recordtypevolumepath** (2) festgelegt werden.

</dd> <dt>

**bytedata**
</dt> <dd>

Der Start einer auf NULL endenden Zeichenfolge, die den Volumepfad angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf diesen Header folgt ein **DWORD** -Wert, der mit dem Wert des **dwrecordsize** -Members von **recordheader** identisch sein sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                            |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                       |



 

 





