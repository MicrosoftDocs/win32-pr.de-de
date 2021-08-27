---
description: Weitere Informationen finden Sie unter Maximale Einstellungen Konstanten.
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
ms.openlocfilehash: fa6ff7044dcd43e4b51c801784d29955f3d34a15
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982223"
---
# <a name="maximum-settings-constants"></a>Maximale Einstellungen Konstanten


_**Gilt für:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Maximale Einstellungen Konstanten

Diese Konstanten stellen die maximal zulässigen Einstellungen für Elemente in einer ESE-Datenbank zur Verfügung.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Legt die Länge für das Präfix fest, das zum Benennen von Dateien verwendet wird, die von der Datenbank-Engine verwendet werden. Diese Länge gilt für den <a href="gg269235(v=exchg.10).md"></a> Namen, der für den JET_paramBaseName system-Parameter festgelegt ist.</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Legt die maximale Länge <a href="gg269340(v=exchg.10).md">für</a>JET_SIGNATURE.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Die maximale Standardgröße eines Lesezeichens. Dies ist gültig, wenn die Schlüsselgröße beim Standardwert be bleibt.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Die maximale Größe eines Lesezeichens, wenn esent so konfiguriert ist, dass es die größtmöglichen Schlüssel hat.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost wird in Windows 7 eingeführt.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Die maximale Länge eines Objekts, einer Spalte, eines Index oder eines Eigenschaftennamens.</p><p><strong>Hinweis:</strong>  Bei Unicode ist der Wert 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>Die maximale Länge eines "name.name.name..." Erstellen.</p><p><strong>Hinweis:</strong>  Bei Unicode ist der Wert 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Diese Zahl kann verwendet werden, um die maximale Menge eines BLOB zu berechnen, die von der Datenbank-Engine auf einer einzelnen Datenbankseite gespeichert werden kann. Die Formel ist max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</p><p>Dieser Wert ist jetzt veraltet. Die Long-Value-Blockgröße sollte mit dem Parameter JET_paramLVChunkSizeMost werden.</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Die maximale Größe von Nicht-Long-Wert-Spaltendaten.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Die maximale Größe eines Long-Value-Spalten-Standardwerts (LongBinary oder LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Die maximale Standardgröße eines Sortier- oder Indexschlüssels.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Die maximal konfigurierbare Größe eines Sortier- oder Indexschlüssels für eine beliebige Seitengröße. (Siehe JET_INDEXCREATE2.cbKeyMost)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost wird im Betriebssystem Windows 7 eingeführt.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>Die maximal zulässige maximale konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 2048 Byteseiten. Weitere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie unter .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage wird im Betriebssystem Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>Die maximal zulässige maximal konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 4096 Byteseiten. Weitere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie unter .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>Die maximal zulässige maximal konfigurierbare Größe für einen Indexschlüssel in einer Datenbank mit 8192 Byteseiten. Weitere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie unter .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Die minimale zulässige maximale Größe für einen Indexschlüssel. Weitere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie unter .</p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin wird in Windows Vista eingeführt.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Die maximale Schlüsselgröße, wenn der Schlüssel mithilfe eines <em>Grenzwert-Grbits</em>gebildet wird, z. B. JET_bitStrLimit, das in der <a href="gg269329(v=exchg.10).md">JetMakeKey-Funktion verwendet</a> wird.</p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Die maximale Größe des primären Indexes. Dies ist jetzt veraltet.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Die maximale Größe des sekundären Indexes. Dies ist jetzt veraltet.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Die maximale Anzahl von Komponenten in einem Sortier- oder Indexschlüssel.</p><p><strong>Windows Vista:</strong> In Windows Vista und neueren Versionen von Windows der Wert 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Die maximale Anzahl von Spalten, die in einer Tabelle zulässig sind.</p><p><strong>Windows XP:</strong> Der Wert 0x0000fee0 wird in Windows XP und neueren und späteren Versionen von Windows</p><p><strong>Windows 2000:</strong> Der Wert 0x00007ffe wird in 2000 Windows verwendet.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>Die maximale Anzahl fester Spalten, die in einer Tabelle zulässig sind, derzeit 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Die maximale Anzahl von Spalten variabler Länge, die in einer Tabelle enthalten sein können, derzeit 128.</p> | 
| <p>JET_ccolTaggedMost<br />( JET_ccolMost – 0x000000ff )</p> | <p>Die maximale Anzahl markierter Spalten, die in einer Tabelle enthalten sein können(derzeit 64993).</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 


