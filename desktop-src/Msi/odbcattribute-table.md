---
description: Die ODBCAttribute-Tabelle enthält Informationen zu den Attributen Open Database Connectivity (ODBC)-Treibern und Translators.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: ODBCAttribute-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943178"
---
# <a name="odbcattribute-table"></a>ODBCAttribute-Tabelle

Die ODBCAttribute-Tabelle enthält Informationen zu den Attributen Open Database Connectivity (ODBC)-Treibern und Translators.

Die ODBCAttribute-Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Treiber\_  | [Identifier](identifier.md) | J   | N        |
| attribute | [Text](text.md)             | J   | N        |
| Wert     | [Formatiert](formatted.md)   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Treiber\_
</dt> <dd>

Interner Tokenname für einen Treiber. Ein Primärschlüssel für die Tabelle. Ein Fremdschlüssel in der [ODBCDriver-Tabelle](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Name des Treiberattributs. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Lokalisierbarer Zeichenfolgenwert für das Attribut.

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

 

 



