---
description: 'Weitere Informationen zu: Maximale Einstellungen Konstanten'
title: Maximale Einstellungen Konstanten
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38184176e5803cfd22d7b63f9d85e5b62f7ecff1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478966"
---
# <a name="maximum-settings-constants"></a>Maximale Einstellungen Konstanten


_**Gilt für:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Maximale Einstellungen Konstanten

Diese Konstanten stellen die maximalen Einstellungen bereit, die für Elemente in einer ESE-Datenbank zulässig sind.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Legt die Länge für das Präfix fest, das zum Benennen von Dateien verwendet wird, die von der Datenbank-Engine verwendet werden. Diese Länge gilt für den Namen, der für den <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> Systemparameter festgelegt wurde.</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Legt die maximale Länge für <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>fest.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Die maximale Standardgröße eines Lesezeichens. Dies ist gültig, wenn die Schlüsselgröße bei ihrem Standardwert belassen wird.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Die maximale Größe eines Lesezeichens, wenn esent so konfiguriert ist, dass es die größtmöglichen Schlüssel hat.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost wird in Windows 7 eingeführt.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Die maximale Länge eines Objekts, einer Spalte, eines Indexes oder eines Eigenschaftennamens.</p><p><strong>Hinweis</strong>  Bei Unicode ist der Wert 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>Die maximale Länge eines "name.name.name..." Erstellen.</p><p><strong>Hinweis</strong>  Bei Unicode ist der Wert 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Diese Zahl kann verwendet werden, um die maximale Menge eines BLOB zu berechnen, die von der Datenbank-Engine auf einer einzelnen Datenbankseite gespeichert werden kann. Die Formel ist max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</p><p>Dieser Wert ist jetzt veraltet. Die Längenwert-Blockgröße sollte mit dem parameter JET_paramLVChunkSizeMost abgerufen werden.</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Die maximale Größe von Spaltendaten ohne langen Wert.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Die maximale Größe des Standardwerts einer Long-Value-Spalte (LongBinary oder LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Die maximale Standardgröße eines Sortier- oder Indexschlüssels.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Die maximal konfigurierbare Größe eines Sortier- oder Indexschlüssels für jede Seitengröße. (Siehe JET_INDEXCREATE2.cbKeyMost)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost wird im Betriebssystem Windows 7 eingeführt.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>Die maximal zulässige maximal konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 2048 Byteseiten. Weitere Informationen finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE.</a></p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage wird im Betriebssystem Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>Die maximal zulässige maximal konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 4096 Byteseiten. Weitere Informationen finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE.</a></p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>Die maximal zulässige maximal konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 8192 Byteseiten. Weitere Informationen finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE.</a></p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Die maximal zulässige Mindestgröße für einen Indexschlüssel. Weitere Informationen finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE.</a></p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Die maximale Schlüsselgröße, wenn der Schlüssel mithilfe eines <em>grbit-Grenzwerts</em>wie JET_bitStrLimit gebildet wird, der in der <a href="gg269329(v=exchg.10).md">JetMakeKey-Funktion</a> verwendet wird.</p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Die maximale Größe des primären Indexes. Dies ist jetzt veraltet.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Die maximale Größe des sekundären Indexes. Dies ist jetzt veraltet.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Die maximale Anzahl von Komponenten in einem Sortier- oder Indexschlüssel.</p><p><strong>Windows Vista:</strong> In Windows Vista und neueren Versionen von Windows ist der Wert 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Die maximale Anzahl von Spalten, die in einer Tabelle zulässig sind.</p><p><strong>Windows XP:</strong> Der Wert 0x0000fee0 wird in Windows XP und neueren Versionen von Windows</p><p><strong>Windows 2000:</strong> Der Wert 0x00007ffe wird in Windows 2000 verwendet.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>Die maximale Anzahl fester Spalten, die in einer Tabelle zulässig sind(derzeit 127).</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Die maximale Anzahl von Spalten variabler Länge, die in einer Tabelle enthalten sein können(derzeit 128).</p> | 
| <p>JET_ccolTaggedMost<br />( JET_ccolMost – 0x000000ff )</p> | <p>Die maximale Anzahl von markierten Spalten, die in einer Tabelle enthalten sein können, derzeit 64993.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


