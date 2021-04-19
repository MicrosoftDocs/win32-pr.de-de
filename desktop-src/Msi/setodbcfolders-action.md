---
description: Die Aktion setodbcfolders überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: "\"Stodbcfolders\"-Aktion"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343233"
---
# <a name="setodbcfolders-action"></a>"Stodbcfolders"-Aktion

Die Aktion setodbcfolders überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die "stodbcfolders"-Aktion muss nach der " [costfinalize](costfinalize-action.md) "-Aktion und vor der [InstallValidate-Aktion](installvalidate-action.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers.                                            |
| \[2\] | Ursprünglicher Ordner Speicherort des neuen Treibers.                                         |
| \[3\] | Neuer Speicherort des Ordners für den neuen Treiber. Dies ist der Speicherort eines vorhandenen Treibers. |



 

## <a name="remarks"></a>Bemerkungen

Durch diese Aktion wird ein neuer Treiber in demselben Verzeichnis wie der vorhandene Treiber platziert, der ersetzt wird. Die setodbcfolders-Aktion verwendet die [Verzeichnis Tabelle](directory-table.md) , um die Speicherorte vorhandener Treiber festzulegen, die ersetzt werden sollen.

 

 



