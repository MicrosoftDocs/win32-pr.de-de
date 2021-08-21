---
description: Die \_ Columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spaltenkatalog enthält. Es werden die Spalten für alle Tabellen aufgeführt. Sie können diese Tabelle abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cbb603c077d7873cdfbea88070e555902883ba579b422627b2581aca04745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640475"
---
# <a name="_columns-table"></a>\_Spaltentabelle

Die \_ Columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spaltenkatalog enthält. Es werden die Spalten für alle Tabellen aufgeführt. Sie können diese Tabelle abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.

Die \_ Tabelle Columns enthält die folgenden Spalten.



| Spalte | Typ                   | Key | Nullwerte zulässig |
|--------|------------------------|-----|----------|
| Tabelle  | [Text](text.md)       | J   | N        |
| Number | [Integer](integer.md) | J   | N        |
| Name   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Der Name der Tabelle, die die Spalte enthält.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Anzahl
</dt> <dd>

Die Reihenfolge der Spalte innerhalb der Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Der Name der Spalte.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Da die Columns-Tabelle eine Systemtabelle ist, die nicht über SQL-Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der \_ [**MsiDatabaseGetPrimaryKeys-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) oder der [**PrimaryKeys-Eigenschaft abrufen.**](database-primarykeys.md)

In der Tabelle Spalten werden nur \_ persistente Spalten gespeichert. Um zu ermitteln, ob eine temporäre Spalte vorhanden ist, müssten Sie eine Sicht mithilfe einer SELECT-Anweisung für die Tabelle erstellen und dann alle Felder in einem Datensatz durchschleifen, der von der \* [**MsiViewGetColumnInfo-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) mit der OPTION MSICOLINFO NAMES zurückgegeben \_ wird.

 

 



