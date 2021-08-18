---
description: Die SetODBCFolders-Aktion überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: SetODBCFolders-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628640"
---
# <a name="setodbcfolders-action"></a>SetODBCFolders-Aktion

Die SetODBCFolders-Aktion überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die SetODBCFolders-Aktion muss nach der [CostFinalize-Aktion](costfinalize-action.md) und vor der [InstallValidate-Aktion](installvalidate-action.md)erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Beschreibung des Treibers. Der ODBC-Treiberschlüssel.                                            |
| \[2\] | Der ursprüngliche Ordnerspeicherort des neuen Treibers.                                         |
| \[3\] | Neuer Ordnerspeicherort für den neuen Treiber. Dies ist der Speicherort eines vorhandenen Treibers. |



 

## <a name="remarks"></a>Hinweise

Durch diese Aktion wird ein neuer Treiber in dasselbe Verzeichnis platziert wie der vorhandene Treiber, der ersetzt wird. Die Aktion SetODBCFolders verwendet die [Verzeichnistabelle,](directory-table.md) um die Speicherorte vorhandener Treiber festzulegen, die ersetzt werden sollen.

 

 



