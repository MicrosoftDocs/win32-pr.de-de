---
description: 'Weitere Informationen finden Sie hier: JET_COLTYP'
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
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868064"
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
<th><p>BESCHREIBUNG</p></th>
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
<td><p>Ein Spaltentyp, der drei Werte zulässt: <strong>true</strong>, <strong>false</strong>oder <strong>null</strong>. Dieser Spaltentyp ist ein Byte lang und hat eine Größe mit fester Größe. <strong>False</strong> sortiert vor <strong>true</strong>. Beachten Sie, dass die Größe dieses Typs nicht mit der Größe des Varianten booleschen Typs identisch ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Eine 1-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 255 annehmen kann.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Eine 2-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-32768 und 32767 annehmen kann. Negative Werte werden vor positiven Werten sortiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Eine 4-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-2147483648 und 2147483647 annehmen kann. Negative Werte werden vor positiven Werten sortiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-9.223.372.036.854.775.808 und 9223372036854775807 annehmen kann. Negative Werte werden vor positiven Werten sortiert. Dieser Spaltentyp ist mit dem Variant-Währungstyp identisch. Dieser Spaltentyp kann auch als Native 8-Byte-Ganzzahl mit Vorzeichen verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Eine Gleit Komma Zahl mit einfacher Genauigkeit (4 Bytes).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Eine Gleit Komma Zahl mit doppelter Genauigkeit (8 Byte).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Eine Gleit Komma Zahl mit doppelter Genauigkeit (8 Byte), die ein Datum in Bruchteilen von Tagen seit dem Jahr 1900 darstellt. Dieser Spaltentyp ist mit dem Variant-Datentyp identisch.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Eine Spalte mit fester oder variabler Länge, binäre binäre Spalte, die bis zu 255 Bytes lang sein kann.</p>
<p>Dieser Spaltentyp kann verwendet werden, um eine GUID zu implementieren, wenn Sie als 16-Byte-Binär Spalte mit fester Länge konfiguriert ist. Der einzige Nachteil besteht darin, dass die relative Reihenfolge der Werte in einem Index über eine solche Spalte nicht mit der relativen Reihenfolge des standardmäßigen Registrierungs Zeichenfolgen-Renderings einer GUID ( &quot; d. h. {0d6cec99-3F &quot; .</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Eine Text Spalte mit fester oder variabler Länge, die bis zu 255 ASCII-Zeichen lang sein kann oder 127 Unicode-Zeichen lang sein kann.</p>
<p>Alle Zeichen folgen werden als gezählte Anzahl von Zeichen gespeichert. Die Zeichen folgen müssen nicht auf Null enden. Außerdem ist es nicht erforderlich, dass die Anzahl ein NULL-Terminator einschließt. Schließlich können eingebettete NULL-Zeichen gespeichert werden.</p>
<p>ASCII-Zeichen folgen werden für Sortier-und Suchzwecke immer als groß-und Kleinschreibung behandelt. Außerdem werden nur die Zeichen, die dem ersten NULL-Zeichen (sofern vorhanden) vorangestellt sind, für das Sortieren und suchen berücksichtigt.</p>
<p>Unicode-Zeichen folgen verwenden die Win32-API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> , um Sortierschlüssel zu erstellen, die anschließend zum Sortieren und Durchsuchen dieser Daten verwendet werden. Standardmäßig werden Unicode-Zeichen folgen als im US-englischen Gebiets Schema betrachtet und mithilfe der folgenden normalisierungs Flags sortiert und durchsucht: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. In Windows 2000 ist es möglich, diese Flags pro Index anzupassen, damit Sie auch NORM_IGNORENONSPACE enthalten. In Windows XP und höheren Versionen ist es möglich, eine beliebige Kombination der folgenden normalisierungs Flags pro Index anzufordern: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH und SORT_STRINGSORT.</p>
<p>In allen Releases ist es möglich, das Gebiets Schema pro Index anzupassen. Jedes Gebiets Schema kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde. Schließlich werden alle in einer Unicode-Zeichenfolge gefundenen NULL-Zeichen vollständig ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Eine Spalte mit fester oder variabler Länge, binäre binäre Spalte, die bis zu 2147483647 Bytes lang sein kann. Dieser Typ wird als Long-Wert angesehen. Ein langer Wert ist ein spezieller Wert, da er sehr groß sein kann und als Stream auf ihn zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Eine Spalte mit fester oder variabler Länge, eine Text Spalte, die bis zu 2147483647 ASCII-Zeichen lang sein kann oder 1073741823 Unicode-Zeichen lang sein kann. Dieser Typ wird als Long-Wert angesehen. Ein langer Wert ist ein spezieller Wert, da er sehr groß sein kann und als Stream auf ihn zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Dieser Spaltentyp ist veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Eine 4-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 4294967295 annehmen kann.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen-9.223.372.036.854.775.808 und 9223372036854775807 annehmen kann. Negative Werte werden vor positiven Werten sortiert.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Eine binäre Spalte mit einer Länge von 16 Bytes mit fester Länge, die den GUID-Datentyp nativ darstellt. GUID-Spaltenwerte werden auf die gleiche Weise sortiert, wie diese Werte im Standardformat (d. h. {4999b5c0-7657-42d9-bdc1-4b779784e013}) als Zeichen folgen sortiert werden.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Eine 2-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 und 65535 annehmen kann.</p>
<p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und neueren Versionen unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Eine-Konstante, die den maximalen (d. h. einen über den größten gültigen) Spaltentyp beschreibt, der von der Engine unterstützt wird</p>
<p>Dieser Wert sollte mit Bedacht verwendet werden, da er sich ändert, wenn neue Spaltentypen unterstützt werden. Beispielsweise hat Sie unter Windows 2000 einen anderen Literalwert als in Windows XP und höheren Versionen.</p></td>
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


### <a name="see-also"></a>Weitere Informationen

[Jetaddcolumn](./jetaddcolumn-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)
