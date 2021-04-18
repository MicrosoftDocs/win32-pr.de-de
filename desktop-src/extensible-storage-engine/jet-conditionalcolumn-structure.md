---
description: 'Weitere Informationen finden Sie hier: JET_CONDITIONALCOLUMN Struktur'
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343362"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN Struktur

Die **JET_CONDITIONALCOLUMN** Struktur definiert, wie die bedingte Indizierung für einen bestimmten Index ausgeführt wird. Ein bedingter Index enthält einen Index Eintrag für nur die Zeilen, die der angegebenen Bedingung entsprechen. Die bedingte Spalte ist jedoch nicht Teil des Index Schlüssels, sondern nur das vorhanden sein des Index Eintrags.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Member

**cbStruct**

Dieses Feld muss mit sizeof (JET_CONDITIONALCOLUMN) initialisiert werden (in Bytes).

**szcolumnname**

Der Name der Spalte, die die Daten enthält, auf denen die Datenbank-Engine die Zeile bedingt indiziert.

**grbit** Eine Gruppe von Bits, die die Optionen für den bedingten Index enthält. Das übergeben von NULL-oder logisch-**oder** Ed-Werten ist für **JET_CONDITIONALCOLUMN** ungültig. Das Bitfeld muss genau eines der folgenden sein:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>Die durch den <em>szcolumnname</em> -Parameter angegebene Spalte muss NULL sein, damit ein Index Eintrag für eine bestimmte Zeile in diesem Index angezeigt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>Die vom <em>szcolumnname</em> -Parameter angegebene Spalte muss für einen Index Eintrag ungleich NULL sein, damit eine bestimmte Zeile in diesem Index angezeigt wird.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Bemerkungen

Ein bedingter Index enthält einen Index Eintrag für nur die Zeilen, die der angegebenen Bedingung entsprechen. Beispielsweise kann eine Spalte mit dem Namen "markiert" benannt werden, und wenn eine Zeile markiert ist, wird die Spalte auf einen Wert festgelegt, der nicht NULL ist. Mit einem JET_bitIndexColumnMustBeNonNull bedingten Index für diese Spalte werden alle Zeilen angezeigt, die als gekennzeichnet sind, und ein JET_bitIndexColumnMustBeNull bedingter Index zeigt Zeilen an, die nicht als markiert sind. Dies ist auch eine bequeme Möglichkeit zum Löschen von Flags und zum Garbage Collection-Index.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) und <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
