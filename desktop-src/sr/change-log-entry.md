---
title: CHANGE_LOG_ENTRY Struktur
description: Ein Änderungsprotokoll Eintrag.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- CHANGE_LOG_ENTRY Struktur System Wiederherstellung
- PCHANGE_LOG_ENTRY Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040250"
---
# <a name="change_log_entry-structure"></a>\_Struktur der Protokoll \_ Einträge ändern

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

Ein Änderungsprotokoll Eintrag.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**Recordheader**
</dt> <dd>

Eine [**Daten Satz \_ Header**](record-header.md) -Struktur. Der **dwrecordtype** -Member sollte auf **recordtypelogentry** (1) festgelegt werden.

</dd> <dt>

**dwmagicnum**
</dt> <dd>

Dieser Member sollte auf 0xabcdef12 festgelegt werden.

</dd> <dt>

**dwentrytype**
</dt> <dd>

Dieser Member kann einen der folgenden Werte aufweisen:

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

Change \_ \_ logentrytypes \_ aclchange * * (0x2) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

Change \_ \_ logentrytypes \_ attrchange * * (0x4) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

Change \_ \_ logentrytypes \_ dircreate * * (0x80) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

Change \_ \_ logentrytypes \_ dirrename * * (0x100) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

Change \_ \_ logentrytypes \_ dirdelete * * (0x200) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

Change \_ \_ logentrytypes \_ filecreate * * (0x20) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

Change \_ \_ logentrytypes \_ filedelete * * (0x10) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

Change \_ \_ logentrytypes \_ filerename * * (0x40) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

Change \_ \_ logentrytypes \_ inprecreate * * (0x100000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

Change \_ \_ logentrytypes \_ isDir * * (0x20000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

Change \_ \_ logentrytypes \_ isnotdir * * (0x40000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

Change \_ \_ logentrytypes \_ mountcreate * * (0x400) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

Change \_ \_ logentrytypes \_ mountdelete * * (0x800) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

Change \_ \_ logentrytypes \_ nooptimiert * * (0x10000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

Change \_ \_ logentrytypes \_ openbyid * * (0x200000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

Change \_ \_ logentrytypes \_ simulatedelete * * (0x80000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

Change \_ \_ logentrytypes \_ streamchange * * (0x1) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

Change \_ \_ logentrytypes \_ streamcreate * * (0x2000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

Change \_ \_ logentrytypes \_ streamüberschreit * * (0x8) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

Change \_ \_ logentrytypes \_ volumeerror * * (0x1000) * *
</dt> </dl> </dd> <dt>

**dwentryflags**
</dt> <dd>

Dieser Member kann einen der folgenden Werte aufweisen:

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

**Changesets- \_ \_ \_ aclinfo ändern (0x4)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

**Change \_ \_ logentryflags \_ debuginfo (0x8)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

**Change \_ \_ logentryflags \_ secondpath (0x2)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

**Changesetflags- \_ \_ \_ Kurzname ändern (0x10)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

**Change \_ \_ logentryflags \_ TEMPPATH (0x1)**
</dt> </dl> </dd> <dt>

**dwattributes**
</dt> <dd>

Die Dateiattribute der Änderungsprotokoll Datei. Wenn keine Attribute angegeben werden, sollte dieser Wert auf "0xffffffff" festgelegt werden.

</dd> <dt>

**i64SequenceNum**
</dt> <dd>

Die Sequenznummer, die dem Änderungsprotokoll Eintrag zugewiesen ist.

</dd> <dt>

**szprocname**
</dt> <dd>

Der Name des Prozesses, der die Änderung vornimmt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf diese Struktur folgt eine Variable Anzahl von Datensätzen variabler Länge sowie ein **DWORD** -Wert, der mit dem Wert des **dwrecordsize** -Members von **recordheader** identisch sein sollte.

Die Datensätze variabler Länge bestehen aus einer Daten [**Satz \_ Header**](record-header.md) Struktur sowie aus Daten, die verwendet werden können, um den Änderungsprotokoll Eintrag wiederherzustellen. Das Format der Daten hängt vom Wert des **dwrecordtype** -Members der **Datensatz- \_ Header** Struktur ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                            |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                       |



 

 





