---
description: 'Weitere Informationen zu: JetCompact-Funktion'
title: JetCompact-Funktion
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14e79ceda56658bf8b214fff923c2df17fe8f786
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480466"
---
# <a name="jetcompact-function"></a>JetCompact-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcompact-function"></a>JetCompact-Funktion

Die **JetCompact-Funktion** erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird für die Verwendung in einen optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures gepackt, die für die Indizes bei der Indexerstellung ausgewählt wurden. Auf diese Weise können komprimierte Daten so stark wie möglich gespeichert werden. Alternativ können komprimierte Daten Speicherplatz für nachfolgende Datensatzvergrößerungen oder Indexeinfügungen reservieren.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*szDatabaseSrc*

Die Quelldatenbank, die komprimiert wird.

*szDatabaseDest*

Der Name, der für die komprimierte Datenbank verwendet werden soll.

*pfnStatus*

Eine Rückruffunktion, die regelmäßig über den Datenbank-Compact-Vorgang aufgerufen werden kann, um den Fortschritt zu melden.

*pconvert*

Ein Zeiger, der verwendet wird, um eine alternative ESE-DLL festzulegen, die zum Lesen der Quelldatenbank verwendet werden kann, und um optionale Parameter für einen **JetCompact-Vorgang** bereitzustellen, der eine Datenbank von einem früheren in ein höheres Versionsformat konvertiert. Dieses Feature wurde in Windows Server 2003 eingestellt.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCompactRepair</p> | <p>Wird verwendet, wenn bekannt ist, dass die Quelldatenbank beschädigt ist. Sie ermöglicht eine ganze Reihe neuer Verhaltensweisen, die so viele Daten wie möglich aus der Quelldatenbank speichern sollen. <strong>JetCompact</strong> mit dieser Option gibt möglicherweise JET_errSuccess zurück, kopiert aber nicht alle in der Quelldatenbank erstellten Daten. Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</p> | 
| <p>JET_bitCompactStats</p> | <p>Bewirkt, dass <strong>JetCompact</strong> Statistiken für die Quelldatenbank in eine Datei mit dem Namen DFRGINFO.TXT. Zu den Statistiken gehören der Name jeder Tabelle in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary,</a> die groß genug waren, um getrennt vom Datensatz gespeichert zu werden, die Anzahl der gruppierten Indexblattseiten und die Anzahl der Blattseiten mit langen Werten. Darüber hinaus werden zusammenfassende Statistiken, einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Datenbankkomp compaction erforderlichen Zeit und des temporären Datenbankspeicherplatzes, ebenfalls gedumpt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Ein <em>pconvert-Zeiger</em> ungleich NULL wurde bereitgestellt, aber die verwendete ESE-Version unterstützt das Konvertierungsfeature nicht. Dieses Feature wurde in der Windows Server 2003-Version von ESE entfernt.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInTransaction</p> | <p>Die aufrufende Sitzung befindet sich innerhalb einer Transaktion. <strong>JetCompact</strong> muss von einer Sitzung außerhalb einer Transaktion aufgerufen werden.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird die Quelldatenbank in die Zieldatenbank kopiert. Die Zieldatenbank befindet sich in einem optimalen Zustand, z. B. befinden sich alle Tabellenindizes im angrenzenden logischen Speicherplatz. Jede Indexseite wird auf die Menge aufgefüllt, die bei der ursprünglichen Erstellung der Indizes in der Quelldatenbank konfiguriert wurde. Alle Daten- und Metadateneinstellungen werden mit voller Genauigkeit kopiert, es sei denn, die Reparaturoption wurde angegeben. Wenn die Reparaturoption angegeben wurde, wurden einige Daten aus der Quelldatenbank möglicherweise nicht kopiert.

Bei einem Fehler ist die Zieldatenbank möglicherweise vorhanden, aber keine vollständige Kopie der Quelldatenbank.

#### <a name="remarks"></a>Hinweise

Das Komprimieren einer Datenbank wird auch verwendet, um ein Upgrade einer Datenbank von einem früheren Versionsformat auf eine modernere Version durchzuführen. Ein optionaler Parameter ist *pconvert,* der eine -Struktur enthält, die eine Beschreibung für eine frühere Versions-DLL zum Lesen des Quelldatenbankformats enthalten kann. Dieses Feature wurde in Windows Server 2003 eingestellt. Nach Windows Server 2003 können neue Ese-Versionen immer ältere Versionen des Datenbankformats lesen. Daher ist dieses Feature nicht erforderlich.

Die gewünschte Dichte der Daten nach einem kompakten Vorgang wird angegeben, wenn Tabellen und Indizes erstellt werden. Die Dichte muss zwischen 20 % und 100 % liegen. Wenn eine Datenbank in erster Linie gelesen und nicht aktualisiert wird, legen Anwendungen die Dichte auf 100 % fest, um die Anzahl von E/A-Vorgängen während der Abfrageverarbeitung zu reduzieren. Wenn die Daten jedoch häufig mit Vorgängen aktualisiert werden, die die Größe der zusammen mit dem Datensatz gespeicherten Daten erhöhen, oder wenn häufig neue Daten eingefügt werden, wählt die Anwendung eine geringere Dichte aus, sodass Updates häufiger benötigte Ressourcen finden. Das Komprimieren der Datenbank bewirkt, dass die Datenbank gemäß der von der Anwendung ausgewählten Füllung ideal angeordnet wird.

Die Datenbankkompprimierung ist ein Offlinevorgang. Sie kann nicht ausgeführt werden, während die Datenbank verwendet wird. Daher erfolgt dies in der Regel im Rahmen eines Buildprozesses zur Entwicklung einer Anwendung, die ein Dataset als Teil von sich selbst übermittelt.

Die Komprimierung von Offlinedatenbanken betrifft jedes Datenbit in einer Datenbank und kann zur Überprüfung der Konsistenz einer Datenbank verwendet werden. Wenn eine Datenbank verdächtig ist, kann sie komprimiert werden. Wenn bei der Komprimierung kein Fehler gefunden wird, ist bekannt, dass sich die Datenbank in einem gültigen Zustand für ESE befindet.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetCompactW</strong> (Unicode) und <strong>JetCompactA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
