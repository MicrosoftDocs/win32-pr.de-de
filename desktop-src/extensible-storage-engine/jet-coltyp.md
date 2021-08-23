---
description: 'Weitere Informationen finden Sie unter: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
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
ms.openlocfilehash: cff7faa9b5523a25f9adb83f2d58797d0630dd529777a089faf36b77f9bce385
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668380"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

Die **JET_COLTYP** Gruppe von Konstanten beschreibt alle möglichen Spaltentypen, die in einer Tabelle gefunden werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante/Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Ein ungültiger Spaltentyp.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Ein Spaltentyp, der drei Werte zulässt: <strong>True,</strong> <strong>False</strong>oder <strong>NULL.</strong> Dieser Spaltentyp ist ein Byte lang und hat eine feste Größe. <strong>False</strong> sortiert vor <strong>True.</strong> Beachten Sie, dass die Größe dieses Typs nicht mit der Größe des booleschen Variantentyps überein passt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Eine 1-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 255 übernehmen kann.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Eine 2-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen -32768 und 32767 übernehmen kann. Negative Werte werden vor positiven Werten sortiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Eine 4-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 2147483648 und 2147483647. Negative Werte werden vor positiven Werten sortiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 9223372036854775808 und 9223372036854775807. Negative Werte werden vor positiven Werten sortiert. Dieser Spaltentyp ist mit dem Variantenwährungstyp identisch. Dieser Spaltentyp kann auch als native 8-Byte-Ganzzahl mit Vorzeichen verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Eine Gleitkommazahl mit einzelner Genauigkeit (4 Byte).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Eine Gleitkommazahl mit doppelter Genauigkeit (8 Byte).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Eine Gleitkommazahl mit doppelter Genauigkeit (8 Byte), die ein Datum in Sekundenbruchteilen seit dem Jahr 1900 darstellt. Dieser Spaltentyp ist mit dem Variantendatumstyp identisch.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Eine unformatiert binäre Spalte mit fester oder variabler Länge, die bis zu 255 Byte lang sein kann.</p>
<p>Dieser Spaltentyp kann verwendet werden, um eine GUID zu implementieren, wenn sie als binäre 16-Byte-Spalte mit fester Länge konfiguriert ist. Der einzige Nachteil ist, dass die relative Reihenfolge der Werte in einem Index für eine solche Spalte nicht mit der relativen Reihenfolge des standardmäßigen Renderings von Registrierungszeichenfolgen einer GUID (d. h. &quot; { 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} ) übereinstimmen &quot; wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Eine Textspalte fester oder variabler Länge, die bis zu 255 ASCII-Zeichen oder 127 Unicode-Zeichen lang sein kann.</p>
<p>Alle Zeichenfolgen werden als gezählte Anzahl von Zeichen gespeichert. Die Zeichenfolgen müssen nicht null-terminiert sein. Darüber hinaus ist es nicht erforderlich, dass die Anzahl ein NULL-Abschlusszeichen enthält. Schließlich können eingebettete NULL-Zeichen gespeichert werden.</p>
<p>ASCII-Zeichenfolgen werden für Sortierungs- und Suchzwecke immer als groß-/kleinschreibungsunabhängig behandelt. Darüber hinaus werden nur die Zeichen, die dem ersten NULL-Zeichen voran stehen (sofern dies der Fall ist) für die Sortierung und Suche berücksichtigt.</p>
<p>Unicode-Zeichenfolgen verwenden die Win32-API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString,</a> um Sortierschlüssel zu erstellen, die anschließend zum Sortieren und Durchsuchen dieser Daten verwendet werden. Unicode-Zeichenfolgen werden standardmäßig als im englischen US-Amerikanischen Locale betrachtet und mithilfe der folgenden Normalisierungsflags sortiert und durchsucht: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. In Windows 2000 ist es möglich, diese Flags pro Index so anzupassen, dass sie auch NORM_IGNORENONSPACE. In Windows XP und späteren Versionen ist es möglich, eine beliebige Kombination der folgenden Normalisierungsflags pro Index an fordern: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH und SORT_STRINGSORT.</p>
<p>In allen Releases ist es möglich, das Locale pro Index anzupassen. Ein beliebiges Locale kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde. Schließlich werden alle NULL-Zeichen, die in einer Unicode-Zeichenfolge gefunden werden, vollständig ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Eine unformatiert binäre Spalte mit fester oder variabler Länge, die bis zu 2147483647 Bytes lang sein kann. Dieser Typ wird als Long-Wert betrachtet. Ein Long-Wert ist besonders, da er groß sein kann und auf ihn als Stream zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Eine Textspalte mit fester oder variabler Länge, die bis zu 2147483647 ASCII-Zeichen lang oder 1073741823 Unicode-Zeichen lang sein kann. Dieser Typ wird als Long-Wert betrachtet. Ein Long-Wert ist besonders, da er groß sein kann und auf ihn als Stream zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Dieser Spaltentyp ist veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Eine 4-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 4294967295.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 9223372036854775808 und 9223372036854775807. Negative Werte werden vor positiven Werten sortiert.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Eine binäre Spalte mit fester Länge von 16 Byte, die den GUID-Datentyp nativ darstellt. GUID-Spaltenwerte werden in der gleichen Weise sortiert wie diese Werte als Zeichenfolgen in Standardform (d.h. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Eine 2-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 und 65535 übernehmen kann.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Eine Konstante, die den maximalen (d. h. einen über den größten gültigen) Spaltentyp hinaus beschreibt, der von der Engine unterstützt wird.</p>
<p>Dieser Wert sollte mit Vorsicht verwendet werden, da er sich ändert, wenn neue Spaltentypen unterstützt werden. Beispielsweise hat sie einen anderen Literalwert für Windows 2000 als bei Windows XP und späteren Versionen.</p></td>
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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
