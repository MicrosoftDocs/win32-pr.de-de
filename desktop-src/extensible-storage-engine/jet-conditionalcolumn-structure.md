---
description: 'Weitere Informationen finden Sie unter: JET_CONDITIONALCOLUMN Struktur'
title: JET_CONDITIONALCOLUMN Struktur
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: dacaff181b40af870bd01bf9d287683c3d3d63a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469477"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN Struktur

Die **JET_CONDITIONALCOLUMN** definiert, wie die bedingte Indizierung für einen bestimmten Index ausgeführt wird. Ein bedingter Index enthält einen Indexeintrag nur für die Zeilen, die mit der angegebenen Bedingung übereinstimmen. Die bedingte Spalte ist jedoch nicht Teil des Indexschlüssels, sondern steuert nur das Vorhandensein des Indexeintrags.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Member

**cbStruct**

Dieses Feld muss mit sizeof( JET_CONDITIONALCOLUMN ) in Bytes initialisiert werden.

**szColumnName**

Der Name der Spalte, die die Daten enthält, für die die Datenbank-Engine die Zeile bedingt indiziert.

**grbit** Eine Gruppe von Bits, die die Optionen für den bedingten Index angibt. Die Übergabe von Null- oder **logisch-OR-Werten** ist für **JET_CONDITIONALCOLUMN.** Das Bitfeld muss genau eines der folgenden Sein:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitIndexColumnMustBeNull</p> | <p>Die durch den <em>szColumnName-Parameter</em> angegebene Spalte muss NULL sein, damit ein Indexeintrag für eine bestimmte Zeile in diesem Index angezeigt wird.</p> | 
| <p>JET_bitIndexColumnMustBeNonNull</p> | <p>Die durch den <em>szColumnName-Parameter</em> angegebene Spalte muss für einen Indexeintrag nicht NULL sein, damit eine bestimmte Zeile in diesem Index angezeigt wird.</p> | 



### <a name="remarks"></a>Hinweise

Ein bedingter Index enthält einen Indexeintrag nur für die Zeilen, die mit der angegebenen Bedingung übereinstimmen. Beispielsweise könnte eine Spalte den Namen "Marked" haben, und wenn eine Zeile markiert ist, wird die Spalte auf einen Wert festgelegt, der nicht NULL ist. Ein JET_bitIndexColumnMustBeNonNull index für diese Spalte zeigt alle markierten Zeilen an, und ein JET_bitIndexColumnMustBeNull bedingter Index zeigt Zeilen an, die nicht markiert sind. Dies ist auch eine praktische Möglichkeit zum Löschen eines Flags und zum Garbage Collection-Index.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) und JET_CONDITIONALCOLUMN_A (ANSI) implementiert. <strong></strong></p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
