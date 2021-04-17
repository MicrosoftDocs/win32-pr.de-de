---
description: Weitere Informationen finden Sie in der jetbeginexternalbackupinstance-Funktion.
title: Jetbeginexternalbackupinstance-Funktion
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
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484243"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Jetbeginexternalbackupinstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginexternalbackupinstance-function"></a>Jetbeginexternalbackupinstance-Funktion

Die **jetbeginexternalbackupinstance** -Funktion initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind.

**Windows XP: jetbeginexternalbackupinstance** wurde in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die Daten Bank Instanz, die für diesen-Befehl verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Dieses Flag ist veraltet. Die Verwendung dieses Bits führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung. Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Für die zukünftige Verwendung reserviert. Definiert für Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Das System generiert möglicherweise Erfolgs-oder Fehlercodes, wenn diese Funktion aufgerufen wird. Eine umfassende Liste der Fehler für diese API finden Sie unter [Fehler Codes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md).

Siehe [jetbeginexternalbackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Bemerkungen

**Jetbeginexternalbackupinstance** ist die erste Funktion in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen. Siehe auch [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) und [jetstopbackupinstance](./jetstopbackupinstance-function.md).

Eine externe Sicherung kann zum Implementieren von vollständigen, inkrementellen oder differenziellen Sicherungen verwendet werden.

Bei der Sicherung handelt es sich um einen fuzzywert, da die Sicherung zu einem bestimmten Zeitpunkt im Transaktionsverlauf konsistent ist, aber das Steuern des genauen Zeitpunkts ist zurzeit nicht möglich.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetattachdatabase](./jetattachdatabase-function.md)  
[Jetbeginexternalbackup](./jetbeginexternalbackup-function.md)  
[Jetclosefile](./jetclosefile-function.md)  
[Jetendexternalbackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[Jetgetattachinfo](./jetgetattachinfo-function.md)  
[Jetgetloginfo](./jetgetloginfo-function.md)  
[Jetopumfile](./jetopenfile-function.md)  
[Jetreadfile](./jetreadfile-function.md)  
[Jetstopbackup](./jetstopbackup-function.md)  
[Jettruneurelog](./jettruncatelog-function.md)
