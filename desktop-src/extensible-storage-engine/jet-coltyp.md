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
ms.openlocfilehash: d4a7433b6e2882a90c9c6fdfe0180b5f5ab7a8e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476876"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

Die **JET_COLTYP** Gruppe von Konstanten beschreibt alle möglichen Spaltentypen, die in einer Tabelle gefunden werden können.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_coltypNil<br />0</p> | <p>Ein ungültiger Spaltentyp.</p> | 
| <p>JET_coltypBit<br />1</p> | <p>Ein Spaltentyp, der drei Werte zulässt: <strong>True,</strong> <strong>False</strong>oder <strong>NULL.</strong> Dieser Spaltentyp ist ein Byte lang und hat eine feste Größe. <strong>False</strong> sortiert vor <strong>True.</strong> Beachten Sie, dass die Größe dieses Typs nicht mit der Größe des booleschen Variantentyps überein passt.</p> | 
| <p>JET_coltypUnsignedByte<br />2</p> | <p>Eine 1-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 255 übernehmen kann.</p> | 
| <p>JET_coltypShort<br />3</p> | <p>Eine 2-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen -32768 und 32767 übernehmen kann. Negative Werte werden vor positiven Werten sortiert.</p> | 
| <p>JET_coltypLong<br />4</p> | <p>Eine 4-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 2147483648 und 2147483647. Negative Werte werden vor positiven Werten sortiert.</p> | 
| <p>JET_coltypCurrency<br />5</p> | <p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 9223372036854775808 und 9223372036854775807. Negative Werte werden vor positiven Werten sortiert. Dieser Spaltentyp ist mit dem Variantenwährungstyp identisch. Dieser Spaltentyp kann auch als native 8-Byte-Ganzzahl mit Vorzeichen verwendet werden.</p> | 
| <p>JET_coltypIEEESingle<br />6</p> | <p>Eine Gleitkommazahl mit einzelner Genauigkeit (4 Byte).</p> | 
| <p>JET_coltypIEEEDouble<br />7</p> | <p>Eine Gleitkommazahl mit doppelter Genauigkeit (8 Byte).</p> | 
| <p>JET_coltypDateTime<br />8</p> | <p>Eine Gleitkommazahl mit doppelter Genauigkeit (8 Byte), die ein Datum in Sekundenbruchteilen seit dem Jahr 1900 darstellt. Dieser Spaltentyp ist mit dem Variantendatumstyp identisch.</p> | 
| <p>JET_coltypBinary<br />9</p> | <p>Eine unformatiert binäre Spalte mit fester oder variabler Länge, die bis zu 255 Byte lang sein kann.</p><p>Dieser Spaltentyp kann verwendet werden, um eine GUID zu implementieren, wenn sie als binäre 16-Byte-Spalte mit fester Länge konfiguriert ist. Der einzige Nachteil ist, dass die relative Reihenfolge der Werte in einem Index für eine solche Spalte nicht mit der relativen Reihenfolge des standardmäßigen Renderings von Registrierungszeichenfolgen einer GUID (d. h. "{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}") übereinstimmen wird.</p> | 
| <p>JET_coltypText<br />10</p> | <p>Eine Textspalte fester oder variabler Länge, die bis zu 255 ASCII-Zeichen oder 127 Unicode-Zeichen lang sein kann.</p><p>Alle Zeichenfolgen werden als gezählte Anzahl von Zeichen gespeichert. Die Zeichenfolgen müssen nicht null-terminiert sein. Darüber hinaus ist es nicht erforderlich, dass die Anzahl ein NULL-Abschlusszeichen enthält. Schließlich können eingebettete NULL-Zeichen gespeichert werden.</p><p>ASCII-Zeichenfolgen werden für Sortierungs- und Suchzwecke immer als groß-/kleinschreibungsunabhängig behandelt. Darüber hinaus werden nur die Zeichen, die dem ersten NULL-Zeichen voran stehen (sofern dies der Fall ist) für die Sortierung und Suche berücksichtigt.</p><p>Unicode-Zeichenfolgen verwenden die Win32-API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString,</a> um Sortierschlüssel zu erstellen, die anschließend zum Sortieren und Durchsuchen dieser Daten verwendet werden. Unicode-Zeichenfolgen werden standardmäßig als im englischen Us-amerikanischen Locale betrachtet und mithilfe der folgenden Normalisierungsflags sortiert und durchsucht: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. In Windows 2000 ist es möglich, diese Flags pro Index so anzupassen, dass sie auch NORM_IGNORENONSPACE. In Windows XP und späteren Versionen ist es möglich, eine beliebige Kombination der folgenden Normalisierungsflags pro Index an fordern: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH und SORT_STRINGSORT.</p><p>In allen Releases ist es möglich, das Locale pro Index anzupassen. Ein beliebiges Locale kann verwendet werden, solange das entsprechende Sprachpaket auf dem Computer installiert wurde. Schließlich werden alle NULL-Zeichen, die in einer Unicode-Zeichenfolge gefunden werden, vollständig ignoriert.</p> | 
| <p>JET_coltypLongBinary<br />11</p> | <p>Eine unformatiert binäre Spalte mit fester oder variabler Länge, die bis zu 2147483647 Bytes lang sein kann. Dieser Typ wird als Long-Wert betrachtet. Ein Long-Wert ist besonders, da er groß sein kann und auf ihn als Stream zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypBinary.</p> | 
| <p>JET_coltypLongText<br />12</p> | <p>Eine Textspalte mit fester oder variabler Länge, die bis zu 2147483647 ASCII-Zeichen lang oder 1073741823 Unicode-Zeichen lang sein kann. Dieser Typ wird als Long-Wert betrachtet. Ein Long-Wert ist besonders, da er groß sein kann und auf ihn als Stream zugegriffen werden kann. Dieser Typ ist andernfalls identisch mit JET_coltypText.</p> | 
| <p>JET_coltypSLV<br />13</p> | <p>Dieser Spaltentyp ist veraltet.</p> | 
| <p>JET_coltypUnsignedLong<br />14</p> | <p>Eine 4-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 (null) und 4294967295.</p><p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p> | 
| <p>JET_coltypLongLong<br />15</p> | <p>Eine 8-Byte-Ganzzahl mit Vorzeichen, die Werte zwischen - 9223372036854775808 und 9223372036854775807. Negative Werte werden vor positiven Werten sortiert.</p><p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p> | 
| <p>JET_coltypGUID<br />16</p> | <p>Eine binäre Spalte mit fester Länge von 16 Byte, die den GUID-Datentyp nativ darstellt. GUID-Spaltenwerte werden in der gleichen Weise sortiert wie diese Werte als Zeichenfolgen in Standardform (d.h. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p><p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p> | 
| <p>JET_coltypUnsignedShort<br />17</p> | <p>Eine 2-Byte-Ganzzahl ohne Vorzeichen, die Werte zwischen 0 und 65535 übernehmen kann.</p><p><strong>Windows Vista und Windows Server 2008:</strong>  Dieser Spaltentyp wird unter Windows Vista, Windows Server 2008 und höher unterstützt.</p> | 
| <p>JET_coltypMax<br />18</p> | <p>Eine Konstante, die den maximalen (d. h. einen über den größten gültigen) Spaltentyp hinaus beschreibt, der von der Engine unterstützt wird.</p><p>Dieser Wert sollte mit Vorsicht verwendet werden, da er sich ändert, wenn neue Spaltentypen unterstützt werden. Beispielsweise hat sie einen anderen Literalwert für Windows 2000 als für Windows XP und höhere Versionen.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
