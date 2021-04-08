---
description: Die Tabellen \_ Tabelle ist eine schreibgeschützte Systemtabelle, in der alle Tabellen in der Datenbank aufgelistet sind. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864544"
---
# <a name="_tables-table"></a>\_Tabelle Tabellen

Die Tabellen \_ Tabelle ist eine schreibgeschützte Systemtabelle, in der alle Tabellen in der Datenbank aufgelistet sind. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.

Die \_ Tabelle Tabellen weist die folgende Spalte auf.



| Spalte | Typ             | Schlüssel | Nullwerte zulässig |
|--------|------------------|-----|----------|
| Name   | [Text](text.md) | J   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name einer der Tabellen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Da die \_ Tabellen Tabelle eine Systemtabelle ist, die nicht über SQL-Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion oder der [**primarykeys-Eigenschaft**](database-primarykeys.md)abrufen.

 

 



