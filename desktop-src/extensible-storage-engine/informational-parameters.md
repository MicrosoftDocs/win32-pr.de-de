---
description: 'Weitere Informationen finden Sie hier: Informations Parameter'
title: Informations Parameter
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753320"
---
# <a name="informational-parameters"></a>Informations Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="informational-parameters"></a>Informations Parameter

Dieses Thema enthält Parameter, die verwendet werden, um Informationen über die Datenbank-Engine verfügbar zu machen.

*JET_paramKeyMost*  
134  

Dieser schreibgeschützte Parameter gibt die maximal zulässige Länge des Index Schlüssels an, die für die aktuelle Datenbankseiten Größe (wie von JET_paramDatabasePageSize konfiguriert) ausgewählt werden kann.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>JET_cbKeyMost4KBytePage</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>255 – 65535</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>–</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>–</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Ab Windows Server 2008 und Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxColtyp*  
131  

Dieser Read Only-Parameter gibt den maximalen [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) für diese Version der Datenbank-Engine zurück. Dieser Wert kann verwendet werden, um die Unterstützung einer bestimmten [JET_COLTYP](./jet-coltyp.md)zu testen. Wenn eine angegebene [JET_COLTYP](./jet-coltyp.md) kleiner als der Wert dieses Parameters ist, wird Sie von der Datenbank-Engine unterstützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>JET_coltypUnsignedShort + 1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 255</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>–</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>–</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Ab Windows Server 2008 und Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramLVChunkSizeMost*  
163  

Schreib geschützter Parameter, der die Segmentgröße mit langem Wert basierend auf der konfigurierten Seitengröße zurückgibt. Wenn ein langer Wert mit mehreren Jet {Set-, retrieve}-Spalten aufrufen gelesen oder geschrieben werden soll, ist die Verwendung eines Puffers, dessen Größe ein Vielfaches der Blockgröße ist, effizienter.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>2 KB Seite = 1966 bytes<br />
4 KB Seite = 4014 bytes<br />
8 KB Seite = 8110 bytes<br />
16-KB-Seite = 4050 bytes<br />
32 KB Seite = 8150 bytes</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p></p></td>
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
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
