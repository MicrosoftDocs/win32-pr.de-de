---
description: 'Weitere Informationen zu: jetresizedatabase-Funktion'
title: Jetresizedatabase-Funktion
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362749"
---
# <a name="jetresizedatabase-function"></a>Jetresizedatabase-Funktion


_**Gilt für:** Windows | Windows Server_

Die **jetresizedatabase** -Funktion erweitert oder verkleinert die Größe einer Datenbank, die derzeit geöffnet ist.

Die **jetresizedatabase** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Die Datenbank, die erweitert wird.

*Verbrauchsgüter*

Die angeforderte Größe der Datenbank in Seiten.

*pcpgactual*

Ein Zeiger auf eine Zahl, die die Größe der Datenbank in Seiten nach dem API-Befehl erhält. Wenn der API-Rückruf fehlschlägt, ist der Inhalt des *pcpgactual* -Parameters nicht definiert.

*grbit*

Eine Gruppe von Bits, die 0 (null) oder mehr der in der folgenden Tabelle aufgeführten Werte angibt.

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
<td><p>JET_bitResizeDatabaseOnlyGrow</p></td>
<td><p>Vergrößern Sie nur die Datenbank. Wenn der Größenänderung die Datenbank verkleinern würde, führen Sie keine Aktion aus.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Auf dem Volume ist nicht genügend freier Speicherplatz vorhanden, um die Vergrößerung auszuführen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p>Von der <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a> -Funktion wurde ein Datei bezogener Fehler zurückgegeben. Weitere Informationen zu anderen Datei bezogenen Fehlern, die zurückgegeben werden können, finden Sie unter <a href="gg269242(v=exchg.10).md">jetsetdatabasesize</a>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Wenn die **jetresizedatabase** -Funktion vor dem Einfügen großer Datenmengen aufgerufen wird, wird die Datenbankdatei in einem Vorgang vergrößert. Dadurch wird die Wahrscheinlichkeit verringert, dass die Datenbankdatei auf Dateisystem Ebene fragmentiert wird. Außerdem wird die Häufigkeit reduziert, mit der die Datenbankdatei vergrößert werden muss. Wenn Sie die Datenbankdatei einmal vergrößern, kann Sie schneller sein, als Sie mehrmals anwachsen.

Informationen zum Festlegen der Größe einer Datenbank, die nicht geöffnet wird, finden Sie unter [jetsetdatabasesize](./jetsetdatabasesize-function.md).

Die Dateigröße stimmt möglicherweise nicht mit der Anzahl der Seiten, die im *pcpgreal* -Parameter zurückgegeben werden, ab. Zwei weitere reservierte Seiten können im *pcpgreal* -Parameter nicht gezählt werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[Jetsetdatabasesize](./jetsetdatabasesize-function.md)
