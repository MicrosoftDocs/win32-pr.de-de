---
description: Mit der Aktion RemoveODBC werden die Datenquellen, Translator und Treiber entfernt, die während der Installation entfernt werden.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: RemoveODBC-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580430"
---
# <a name="removeodbc-action"></a>RemoveODBC-Aktion

Mit der Aktion RemoveODBC werden die Datenquellen, Translator und Treiber entfernt, die während der Installation entfernt werden. Diese Aktion fragt die [ODBCDataSource-Tabelle,](odbcdatasource-table.md)die [ODBCTranslator-Tabelle](odbctranslator-table.md)und die [ODBCDriver-Tabelle](odbcdriver-table.md) für jede Datenquelle, jeden Translator oder Treiber ab, die entfernt werden sollen.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Für jeden installierten Treiber.



| Feld | Beschreibung der Aktionsdaten               |
|-------|------------------------------------------|
| \[1\] | Beschreibung des Treibers. Der ODBC-Treiberschlüssel. |
| \[2\] | Componentid                              |



 

Für jeden installierten Translator.



| Feld | Beschreibung der Aktionsdaten               |
|-------|------------------------------------------|
| \[1\] | Beschreibung des Treibers. Der ODBC-Treiberschlüssel. |
| \[2\] | Componentid                              |



 

Für jede installierte Datenquelle.



| Feld | Beschreibung der Aktionsdaten                              |
|-------|---------------------------------------------------------|
| \[1\] | Beschreibung des Treibers. Der ODBC-Treiberschlüssel.                |
| \[2\] | Componentid                                             |
| \[3\] | Registrierung: SQL \_ REMOVE \_ DSN oder SQL \_ REMOVE SYS \_ \_ DSN |



 

## <a name="remarks"></a>Hinweise

Wenn sowohl die ODBC-Nutzungsanzahl als auch die Dateiverwendungsanzahl 0 (null) werden, wird die Datei entfernt. Die Registrierung hängt von der ODBC-Nutzungsanzahl ab, und das Entfernen von Dateien basiert auf der Schlüsselverweisanzahl für freigegebene DLLs.

 

 



