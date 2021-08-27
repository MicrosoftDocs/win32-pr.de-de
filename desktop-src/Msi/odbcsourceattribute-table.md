---
description: Die ODBCSourceAttribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: ODBCSourceAttribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082710"
---
# <a name="odbcsourceattribute-table"></a>ODBCSourceAttribute-Tabelle

Die ODBCSourceAttribute-Tabelle enthält Informationen zu den Attributen von Datenquellen.

Die ODBCSourceAttribute-Tabelle enthält die folgenden Spalten.



| Spalte       | Typ                         | Key | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Datasource\_ | [Identifier](identifier.md) | J   | N        |
| attribute    | [Text](text.md)             | J   | N        |
| Wert        | [Formatiert](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Datasource\_
</dt> <dd>

Interner Tokenname für die Datenquelle. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Name des Datenquellenattributs. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Der lokalisierbare Zeichenfolgenwert für das Attribut.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen InstallODBC](installodbc-action.md) und [RemoveODBC](removeodbc-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen finden* Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



