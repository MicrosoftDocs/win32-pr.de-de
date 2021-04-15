---
description: Die odbcsourceattribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Odbcsourceattribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525772"
---
# <a name="odbcsourceattribute-table"></a>Odbcsourceattribute-Tabelle

Die odbcsourceattribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.

Die odbcsourceattribute-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| DataSource\_ | [Bezeichner](identifier.md) | J   | N        |
| Attribut    | [Text](text.md)             | J   | N        |
| Wert        | [Großformatige](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_
</dt> <dd>

Interner Tokenname für die Datenquelle. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen
</dt> <dd>

Name des Datenquellen Attributs. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Zeichen folgen Wert für das Attribut.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



