---
description: Die odbingtribute-Tabelle enthält Informationen zu den Attributen der Open Database Connectivity (ODBC)-Treiber und-Konvertierer.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Odbingtribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130285"
---
# <a name="odbcattribute-table"></a>Odbingtribute-Tabelle

Die odbingtribute-Tabelle enthält Informationen zu den Attributen der Open Database Connectivity (ODBC)-Treiber und-Konvertierer.

Die odbingtribute-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Treiber\_  | [Bezeichner](identifier.md) | J   | N        |
| Attribut | [Text](text.md)             | J   | N        |
| Wert     | [Großformatige](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Trei\_
</dt> <dd>

Interner Tokenname für einen Treiber. Ein Primärschlüssel für die Tabelle. Ein Fremdschlüssel in der [odbcdriver-Tabelle](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen
</dt> <dd>

Der Name des Treiber Attributs. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Lokalisier barer Zeichen folgen Wert für das Attribut.

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

 

 



