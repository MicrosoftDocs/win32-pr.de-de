---
description: 'Weitere Informationen zu: JetBeginExternalBackupInstance-Funktion'
title: JetBeginExternalBackupInstance-Funktion
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53583a1d51de390b0c84143dcb59f3327b7c91bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479296"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance-Funktion

Die **JetBeginExternalBackupInstance-Funktion** initiiert eine externe Sicherung, während engine und database online und aktiv sind.

**Windows XP: JetBeginExternalBackupInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Datenbankinstanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und höhere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Dieses Flag ist veraltet. Die Verwendung dieses Bits führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Erstellt eine inkrementelle Sicherung im Gegensatz zu einer vollständigen Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Für die zukünftige Verwendung reserviert. Definiert für Windows XP.</p> | 



### <a name="return-value"></a>Rückgabewert

Das System kann als Ergebnis eines Aufrufs dieser Funktion Erfolgs- oder Fehlercodes generieren. Eine vollständige Liste der Fehler für diese API finden Sie unter [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).

Weitere Informationen finden Sie unter [JetBeginExternalBackup.](./jetbeginexternalbackup-function.md)

#### <a name="remarks"></a>Hinweise

**JetBeginExternalBackupInstance** ist die erste Funktion in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche Onlinesicherung (nicht VSS-basiert) auszuführen. Siehe auch [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) und [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Eine externe Sicherung kann verwendet werden, um vollständige, inkrementelle oder differenzielle Sicherungen zu implementieren.

Die Sicherung ist unscharf, da die Sicherung zu einem einzelnen Zeitpunkt im Transaktionsverlauf konsistent ist, aber das Steuern des genauen Zeitpunkts zu diesem Zeitpunkt nicht möglich ist.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
