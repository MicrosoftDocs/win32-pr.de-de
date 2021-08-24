---
description: Mit der Aktion UnregisterTypeLibraries wird die Registrierung von Typbibliotheken beim System aufgehoben. Diese Aktion wird auf jede Datei angewendet, die in der TypeLib-Tabelle aufgeführt ist, für die die Deinstallation ausgelöst wird.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: UnregisterTypeLibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810120"
---
# <a name="unregistertypelibraries-action"></a>UnregisterTypeLibraries-Aktion

Mit der Aktion UnregisterTypeLibraries wird die Registrierung von Typbibliotheken beim System aufgehoben. Diese Aktion wird auf jede Datei angewendet, die in der [TypeLib-Tabelle](typelib-table.md) aufgeführt ist, für die die Deinstallation ausgelöst wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die UnregisterTypeLibraries-Aktion muss vor der [RemoveFiles-Aktion](removefiles-action.md) erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) einer nicht registrierten Typbibliothek. |



 

 

 



