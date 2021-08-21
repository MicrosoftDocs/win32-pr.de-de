---
description: 'Weitere Informationen finden Sie unter: JET_SETCOLUMN Struktur'
title: JET_SETCOLUMN Struktur
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: ffdcd2ea11fad6c9ec2baae1a37bdd1965acb852
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466367"
---
# <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN Struktur

Die **JET_SETCOLUMN-Struktur** enthält Eingabe- und Ausgabeparameter für [JetSetColumns.](./jetsetcolumns-function.md) Felder in der Struktur beschreiben, welcher Spaltenwert festgelegt werden soll, wie er festgelegt wird und wo die Spaltensatzdaten erhalten werden.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Member

**Columnid**

Der Spaltenbezeichner für eine spalte, die festgelegt werden soll.

**pvData**

Ein Zeiger auf Daten, die in einer Spalte festgelegt werden.

**cbData**

Die Größe der Zuordnung in Bytes, beginnend bei **pvData** in Bytes.

**grbit**

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Fügt Daten an eine Spalte vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">oder</a>JET_coltypLongBinary. Das gleiche Verhalten kann erreicht werden, indem die Größe des vorhandenen long-Werts bestimmt und <strong>ibLongValue</strong> in <strong>psetinfo angegeben wird.</strong> Es ist jedoch einfacher, dieses <em>Grbit</em>zu verwenden, da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Ersetzt den vorhandenen Long-Wert durch die neuen Daten. Wenn diese Option verwendet wird, ist dies so, als ob der vorhandene Long-Wert vor dem Festlegen der neuen Daten auf 0 (null) länge festgelegt wurde.</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Interpretiert den Eingabepuffer als eine ganzzahlige Anzahl von Bytes, die als Länge des long-Werts festgelegt werden soll, der von der angegebenen columnid beschrieben wird, und, sofern angegeben, als Sequenznummer in psetinfo- &gt; itagSequence. Wenn die größe größer als der vorhandene Spaltenwert ist, wird die Spalte um 0 s erweitert. Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Legt einen Wert auf die Länge 0 (null) fest. Normalerweise wird ein Spaltenwert auf NULL festgelegt, indem ein cbMax-Wert von 0 übergeben wird. Für einige Typen, z. B. <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, kann ein Spaltenwert jedoch eine Länge von 0 anstelle von NULL haben, und diese Option wird verwendet, um zwischen NULL und 0 Länge zu unterscheiden.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Erzwingt, dass ein long-Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary,</a>getrennt vom Rest der Datensatzdaten gespeichert wird. Dies tritt normalerweise auf, wenn die Größe des long-Werts verhindert, dass er mit den verbleibenden Datensatzdaten gespeichert wird. Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der Long-Wert separat gespeichert wird. Beachten Sie, dass lange Werte mit einer Größe von vier Byte oder kleiner nicht erzwungen werden können, getrennt zu sein. In solchen Fällen wird die Option ignoriert.</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte. Diese Option vergleicht die Quellspaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte. Diese Option vergleicht die schlüsselnormierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Bewirkt, dass die Spalte bei nachfolgenden Abrufspaltenvorgängen den Standardspaltenwert zurück gibt. Alle vorhandenen Spaltenwerte werden entfernt. Diese Option gilt nur für markierte Spalten, Sparsespalten oder mehrwertige Spalten.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Speichert den long-Wert, Spalten vom <a href="gg269213(v=exchg.10).md">Typ JET_coltypLongText</a> oder JET_coltypeLongBinary, die nach Möglichkeit mit den verbleibenden Datensatzdaten gespeichert werden. Normalerweise werden lange Spalten separat gespeichert, wenn ihre Länge 1.024 Byte überschreitet oder andernfalls dazu führen würde, dass die Datensatzlänge die größenbezogene Größenbeschränkung der Seite überschreitet. Wenn diese Option jedoch festgelegt ist, tritt beim Vorgang zum Festlegen der Spalte ein Fehler auf JET_errColumnTooBig anstatt diesen Spaltenwert getrennt von den verbleibenden Datensatzdaten zu speichern.</p> | 



**ibLongValue**

Der Offset zum ersten Byte, das aus einer Spalte vom Typ abgerufen werden soll, JET_coltypLongBinary [oder](./jet-coltyp.md) [JET_coltypLongText.](./jet-coltyp.md)

**itagSequence**

Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte. Eine **itagSequence** von 0 gibt an, dass der Spaltenwertsatz als neue Instanz einer mehrwertigen Spalte hinzugefügt werden soll.

**Err**

Fehlercodes und Warnungen, die vom Vorgang zum Festlegen der Spalte zurückgegeben wurden.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
