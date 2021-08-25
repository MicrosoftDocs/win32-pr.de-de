---
description: 'Weitere Informationen finden Sie unter: JET_RETRIEVECOLUMN Struktur'
title: JET_RETRIEVECOLUMN-Struktur
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 4f29f3c6a9ca3262b3cd09d726634afd70db9c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471456"
---
# <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN-Struktur

Die **JET_RETRIEVECOLUMN-Struktur** enthält Eingabe- und Ausgabeparameter für [JetRetrizugColumns](./jetretrievecolumns-function.md). Felder in der Struktur beschreiben, welcher Spaltenwert abgerufen werden soll, wie er abgerufen wird und wo Ergebnisse zu speichern sind.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Member

**Columnid**

Der Spaltenbezeichner für die abzurufende Spalte.

**pvData**

Ein Zeiger zum Speichern von Daten, die aus dem Spaltenwert abgerufen werden.

**cbData**

Die Größe der Zuordnung ab **pvData** in Bytes. Beim Vorgang zum Abrufen der Spalte werden nicht mehr Daten in **pvData als** **bei cbData gespeichert.**

**cbActual**

Die Größe der Daten in Bytes, die durch einen Abrufspaltenvorgang abgerufen werden.

**grbit**

Eine Gruppe von Bits, die die Optionen für den Spaltenabruf enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Ruft den geänderten Wert anstelle des ursprünglichen Werts ab. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert abgerufen werden, der noch nicht eingefügt oder aktualisiert wurde, wenn ein Datensatz eingefügt oder aktualisiert wird.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Ruft Nach Möglichkeit Spaltenwerte aus dem Index ab, ohne auf den Datensatz zu zugreifen. Auf diese Weise kann unnötiges Laden von Datensätzen vermieden werden, wenn die benötigten Daten über Indexeinträge selbst verfügbar sind. In Fällen, in denen der ursprüngliche Spaltenwert aufgrund von nicht rückgängig gemachten Transformationen oder Datenschneidungen nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden wie gewohnt abgerufen. Dies ist eine Leistungsoption und sollte nur angegeben werden, wenn der Spaltenwert wahrscheinlich aus dem Index abgerufen werden kann. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten oder primären Index die Datensätze selbst sind. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark auch festgelegt ist.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Ruft Spaltenwerte aus dem Index-Lesezeichen ab und kann sich vom Indexwert unterscheiden, wenn eine Spalte sowohl im primären als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte oder primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex auch festgelegt ist.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Ruft die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagSequence ab. Das itagSequence-Feld wird häufig als Eingabe zum Abrufen von werten spaltenübergreifenden Spalten aus einem Datensatz verwendet. Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Indexeintrag einer bestimmten Sequenznummer zu zuordnen und diese Sequenznummer abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf erfolgen.</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>Ruft NULL-Werte für die mehrwertige Spalte ab. Wenn diese Option nicht angegeben wird, werden die NULL-Werte der mehrwertigen Spalte automatisch übersprungen.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und keine festgelegten Werte für die Spalte im Datensatz enthalten sind. Diese Option wirkt sich nur auf mehrwertige Spalten aus.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Dieses Flag ist nur für die interne Verwendung vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Dieses Flag ist nur für die interne Verwendung vorgesehen und nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p> | 



**ibLongValue**

Der Offset zum ersten Byte, das aus einer Spalte vom Typ JET_coltypLongBinary [oder](./jet-coltyp.md) [JET_coltypLongText.](./jet-coltyp.md)

**itagSequence**

Die Sequenznummer der Werte, die in einer mehrwertigen Spalte enthalten sind. **itagSequence** kann hier im **JET_RETRIEVECOLUMN** 0 sein. Wenn **itagSequence** 0 ist, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben. Der **itagSequence-Wert** 0 kann nicht in Aufrufen von [JetRetrieveColumn verwendet werden.](./jetretrievecolumn-function.md)

**columnidNextTagged**

Die **Columnid** der markierten, mehrwertigen oder Sparsespalte, wenn alle markierten Spalten abgerufen werden, indem 0 als **columnid** an [JetRetrieveColumn übergeben wird.](./jetretrievecolumn-function.md)

**Err**

Fehlercodes und Warnungen, die beim Abrufen der Spalte zurückgegeben werden.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
