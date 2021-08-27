---
description: 'Weitere Informationen zu: JetTerm2-Funktion'
title: JetTerm2-Funktion
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9f8e5f278a0ef3eb44efd64314745d2fed6d89b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466617"
---
# <a name="jetterm2-function"></a>JetTerm2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetterm2-function"></a>JetTerm2-Funktion

Die **JetTerm2-Funktion** initiiert das Herunterfahren einer Instanz, die von [JetInit](./jetinit-function.md)initialisiert wurde.

**JetTerm2** kann auch eine nicht initialisierte Instanz zerstören, die von [JetCreateInstance](./jetcreateinstance-function.md)erstellt wurde.

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

**Windows 2000:**  Dieser Parameter wird ignoriert und sollte immer **NULL** sein.

**Windows XP und höher:**  Dieser Parameter ist überladen. Wenn die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **NULL** sein oder die tatsächliche Instanz enthalten, die von [JetInit](./jetinit-function.md)zurückgegeben wird. Wenn die Engine im Modus mit mehreren Instanzen ausgeführt wird, muss dieser Parameter ein Zeiger auf eine Instanz sein, die mit [JetCreateInstance](./jetcreateinstance-function.md)erstellt wurde.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTermComplete</p> | <p>Fordert an, dass die Instanz sauber heruntergefahren wird. Alle optionalen Bereinigungsarbeiten, die normalerweise zur Laufzeit im Hintergrund ausgeführt werden, werden sofort abgeschlossen.</p> | 
| <p>JET_bitTermAbrupt</p> | <p>Fordert an, dass die Instanz so schnell wie möglich heruntergefahren wird. Alle optionalen Arbeiten, die normalerweise zur Laufzeit im Hintergrund ausgeführt werden, werden abgebrochen.</p><p><strong>Hinweis</strong>  Diese Option kann zu temporärem oder dauerhaftem Speicherplatzverlust in der Datenbank führen. Dieser verlorene Speicherplatz kann immer durch eine Offlinedefragmentierung der Datenbank wiederhergestellt werden.</p> | 
| <p>JET_bitTermStopBackup</p> | <p>Fordert an, dass die Instanz heruntergefahren wird, auch wenn derzeit eine Sicherung ausgeführt wird. Normalerweise würde eine ausstehende Sicherung dazu führen, dass <a href="gg269298(v=exchg.10).md">JetTerm</a> mit JET_errBackupInProgress fehlschlägt. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitTermAbrupt ist.</p> | 
| <p>JET_bitTermDirty</p> | <p>Fordert an, dass die Instanz mit allen angefügten Datenbanken heruntergefahren wird, die sich in einem geänderten Zustand befinden.</p><p>Windows 7: JET_bitTermDirty wird in Windows 7 eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Sicherungsvorgang für die Instanz ausgeführt wird.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameter führte zu einem unerwarteten Ergebnis. Dieser Fehler wird von <a href="gg269298(v=exchg.10).md">JetTerm</a> zurückgegeben, wenn sich die Engine im Modus mit mehreren Instanzen befindet und wenn <em>pinstance</em> auf eine ungültige Instanz verweist.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz heruntergefahren wird.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>Die Instanz kann nicht heruntergefahren werden, da derzeit Sitzungen mit aktiven Transaktionen für die angegebene Instanz vorhanden sind. Dieser Fehler tritt nur auf, wenn die JET_bitTermComplete verwendet wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird die angegebene Instanz heruntergefahren. Das Instanzhandle wird ebenfalls geschlossen und für alle APIs, die ein Instanzhandle verwenden, nicht verfügbar gemacht. Alle anderen Objekte, die der Instanz zugeordnet sind, z. B. Sitzungen, werden ebenfalls geschlossen. Der Status der Prüfpunktdatei, der Transaktionsprotokolldateien und der Datenbankdateien, die an die Instanz angefügt sind, wird während des Herunterfahrens geändert.

Wenn diese Funktion aufgrund eines Verwendungsfehlers fehlschlägt, verbleibt die Instanz in einem initialisierten Zustand, und es ändert sich nichts. Andernfalls wird die Instanz weiterhin wie im Erfolgsfall angegeben heruntergefahren. Der Unterschied besteht darin, dass die Instanz bei der nächsten Initialisierung eine Absturzwiederherstellung durchlaufen muss. Die Engine versucht, so viele Daten wie möglich zu leeren, um die erforderliche Wiederherstellung zu minimieren. Konzeptionell unterscheidet sich ein solcher Fehler von [JetTerm](./jetterm-function.md) nicht von einem Prozessabsturz.

#### <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [JetTerm](./jetterm-function.md).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
