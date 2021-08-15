---
description: Die \_ Tabelle Tabellen ist eine schreibgeschützte Systemtabelle, die alle Tabellen in der Datenbank auflistet. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c251693d89bb23634b222518e98dba270856e672362bcdc9acddd3c0b86c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013318"
---
# <a name="_tables-table"></a>\_Tabellentabelle

Die \_ Tabelle Tabellen ist eine schreibgeschützte Systemtabelle, die alle Tabellen in der Datenbank auflistet. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.

Die \_ Tabelle Tabellen enthält die folgende Spalte.



| Spalte | Typ             | Key | Nullwerte zulässig |
|--------|------------------|-----|----------|
| Name   | [Text](text.md) | J   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Name einer der Tabellen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Da die \_ Tabelle Tabellen eine Systemtabelle ist, die nicht durch SQL Abfragen geändert werden kann, können Sie die Primärschlüssel nicht mit der [**MsiDatabaseGetPrimaryKeys-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) oder der [**PrimaryKeys-Eigenschaft**](database-primarykeys.md)abrufen.

 

 



