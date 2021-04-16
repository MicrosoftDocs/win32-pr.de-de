---
title: RECORD_HEADER Struktur
description: Der Daten Satz Header, der von den Changesets für Änderungs \_ Protokoll \_ und Änderungs \_ Protokoll Header verwendet wird \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- RECORD_HEADER Struktur System Wiederherstellung
- PRECORD_HEADER Struktur Zeiger System Wiederherstellung
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478291"
---
# <a name="record_header-structure"></a>Daten Satz- \_ Header Struktur

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

Der Daten Satz Header, der von den Changesets für [**Änderungs \_ Protokoll \_**](change-log-entry.md) und [**Änderungs \_ Protokoll \_ Header**](change-log-header.md) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**dwrecordsize**
</dt> <dd>

Die Gesamtgröße des Datensatzes, einschließlich des Headers, in Byte.

</dd> <dt>

**dwrecordtype**
</dt> <dd>

Der Datensatztyp. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**Recordtypelogheader**</dt> <dt>0</dt> </dl>     | Der Datensatz ist die Kopfzeile für das Änderungsprotokoll.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**Recordtypelogentry**</dt> <dt>1</dt> </dl>         | Der Datensatz ist der Header für einen Änderungsprotokoll Eintrag.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**Recordtypevolumepath**</dt> <dt>2</dt> </dl> | Bei den Daten handelt es sich um den Volumepfad für den Änderungsprotokoll Eintrag.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**Recordtypefirstpath**</dt> <dt>3</dt> </dl>     | Bei den Daten handelt es sich um den Dateipfad für den Änderungsprotokoll Eintrag.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**Recordtypesecondpath**</dt> <dt>4</dt> </dl> | Die Daten werden verwendet, wenn Änderungsprotokoll Einträge umbenannt werden. in diesem Pfad wird die umbenannte Datei gespeichert.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**Recordtypetemppath**</dt> <dt>5</dt> </dl>         | Die Daten sind der Name der Sicherungsdatei, die zum Wiederherstellen des Änderungsprotokoll Eintrags verwendet wird. Die Sicherungsdateien befinden sich im Ordner "RP *n* ". Der Dateiname weist das folgende Format auf:*xxxxxxx*. *ext*, wobei *xxxxxxx* eine siebenstellige Zahl und *ext* die Dateinamenerweiterung ist.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**Recordtypeaclinline**</dt> <dt>6</dt> </dl>     | Bei den Daten handelt es sich um eine ACL. Das Datenformat ist eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Dieser Wert darf nicht größer als 8.192 Bytes sein. Um einen Wert anzugeben, der größer als 8.192 Byte ist, verwenden Sie den **recordtypeaclfile** -Member.<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**Recordtypeaclfile**</dt> <dt>7</dt> </dl>             | Bei den Daten handelt es sich um den Namen der ACL-Datei, die zum Speichern der ACL verwendet wird. Die ACL-Dateien befinden sich im Ordner "RP *n* ". Der Dateiname hat das folgende Format: S *xxxxxxx*. ACL, wobei *xxxxxxx* eine siebenstellige Zahl ist.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**Recordtypedebuginfo**</dt> <dt>8</dt> </dl>     | Bei den Daten handelt es sich um Debuginformationen für den Änderungsprotokoll Eintrag. Das Datenformat ist eine **SR \_ log \_ Debug \_ Info** -Struktur. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**Recordtypeshortname**</dt> <dt>9</dt> </dl>     | Bei den Daten handelt es sich um den Kurznamen der Sicherungsdatei.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **SR \_ log \_ Debug \_ Info** -Struktur ist wie folgt definiert.

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                            |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                       |



 

