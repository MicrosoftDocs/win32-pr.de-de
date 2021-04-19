---
description: Die \_ columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spalten Katalog enthält. Sie listet die Spalten für alle Tabellen auf. Sie können diese Tabelle Abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356117"
---
# <a name="_columns-table"></a>\_Columns-Tabelle

Die \_ columns-Tabelle ist eine schreibgeschützte Systemtabelle, die den Spalten Katalog enthält. Sie listet die Spalten für alle Tabellen auf. Sie können diese Tabelle Abfragen, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.

Die \_ Spalten Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                   | Schlüssel | Nullwerte zulässig |
|--------|------------------------|-----|----------|
| Tabelle  | [Text](text.md)       | J   | N        |
| Number | [Integer](integer.md) | J   | N        |
| Name   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Der Name der Tabelle, die die Spalte enthält.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Einigen
</dt> <dd>

Die Reihenfolge der Spalte in der Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name der Spalte.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Da die \_ columns-Tabelle eine Systemtabelle ist, die nicht über SQL-Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion oder der [**primarykeys-Eigenschaft**](database-primarykeys.md)abrufen.

Nur persistente Spalten werden in der \_ Spalten Tabelle gespeichert. Wenn Sie ermitteln möchten, ob eine temporäre Spalte vorhanden ist, müssen Sie eine Sicht mit einer SELECT- \* Anweisung für die Tabelle erstellen und dann alle Felder in einem Datensatz durchlaufen, der von der [**msiviewgetcolumninfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) -Funktion mit der msicolinfo Names-Option zurückgegeben wird \_ .

 

 



