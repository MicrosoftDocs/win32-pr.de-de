---
description: 'Weitere Informationen: Konstanten für maximale Einstellungen'
title: Konstanten für maximale Einstellungen
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862891"
---
# <a name="maximum-settings-constants"></a>Konstanten für maximale Einstellungen


_**Gilt für:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Konstanten für maximale Einstellungen

Diese Konstanten stellen die maximalen Einstellungen bereit, die für Elemente in einer ESE-Datenbank zulässig sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante/Wert</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Legt die Länge des Präfixes fest, das zum Benennen von Dateien verwendet wird, die von der Datenbank-Engine verwendet werden. Diese Länge gilt für den Namen, der für den <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> System-Parameter festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Legt die maximale Länge für <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>fest.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>Die standardmäßige maximale Größe eines Lesezeichens. Dies ist gültig, wenn die Schlüsselgröße den Standardwert übersteigt.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>Die maximale Größe eines Lesezeichens, wenn ESENT so konfiguriert ist, dass es die größten möglichen Schlüssel hat.</p>
<p><strong>Windows 7:</strong> JET_cbBookmarkMostMost wurde in Windows 7 eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>Die maximale Länge für ein-Objekt, eine Spalte, einen Index oder einen Eigenschaftsnamen.</p>
<p><strong>Hinweis</strong>  Wenn Unicode, ist der Wert 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>Die maximale Länge eines &quot; Name.Name.Name...- &quot; Konstrukts.</p>
<p><strong>Hinweis</strong>  Wenn Unicode, ist der Wert 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Diese Zahl kann verwendet werden, um die maximale Größe eines BLOBs zu berechnen, das von der Datenbank-Engine auf einer einzelnen Datenbankseite gespeichert werden kann. Die Formel ist Max Size = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p>
<p>Dieser Wert ist mittlerweile veraltet. Die Blockgröße für den langen Wert sollte mit dem JET_paramLVChunkSizeMost-Parameter abgerufen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>Die maximale Größe von Spaltendaten, die keine langen Werte sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>Die maximale Größe eines Standardwerts für eine lange Wert Spalte (LONGBINARY oder LONGTEXT).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>Die standardmäßige maximale Größe eines Sortier-oder Index Schlüssels.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>Die maximal konfigurierbare Größe eines Sortier-oder Index Schlüssels für eine beliebige Seitengröße. (Siehe JET_INDEXCREATE2. cbkeymost)</p>
<p><strong>Windows 7:</strong> JET_cbKeyMostMost wird im Betriebssystem Windows 7 eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 2048-Byte-Seiten. Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage wird im Betriebssystem Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 4096-Byte-Seiten. Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>Die maximal zulässige maximal konfigurierbare Größe für einen Index Schlüssel in einer Datenbank mit 8192-Byte-Seiten. Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>Die minimal zulässige Maximalgröße für einen Index Schlüssel. Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMostMin wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>Die maximale Schlüsselgröße, wenn der Schlüssel mithilfe eines Limit- <em>grbit</em>gebildet wird, z. b. JET_bitStrLimit, das in der <a href="gg269329(v=exchg.10).md">jetmakekey</a> -Funktion verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>Die maximale Größe des primären Indexes. Dies ist mittlerweile veraltet.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>Die maximale Größe des sekundären Indexes. Dies ist mittlerweile veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>Die maximale Anzahl von Komponenten in einem Sortier-oder Index Schlüssel.</p>
<p><strong>Windows Vista:  </strong> In Windows Vista und höheren Versionen von Windows lautet der Wert 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>Die maximal zulässige Anzahl von Spalten in einer Tabelle.</p>
<p><strong>Windows XP:  </strong> Der Wert 0x0000fee0 wird in Windows XP und höheren Versionen von Windows verwendet.</p>
<p><strong>Windows 2000:  </strong> Der Wert 0x00007ffe wird in Windows 2000 verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
0x0000007F</p></td>
<td><p>Die maximal zulässige Anzahl fester Spalten in einer Tabelle, derzeit 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>Die maximale Anzahl von Spalten variabler Länge, die in einer Tabelle enthalten sein können, zurzeit 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000ff)</p></td>
<td><p>Die maximale Anzahl von markierten Spalten, die in einer Tabelle enthalten sein können, zurzeit 64993.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

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
</tbody>
</table>

