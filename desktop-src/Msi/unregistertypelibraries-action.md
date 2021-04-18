---
description: Die unregistertypelibraries-Aktion hebt die Registrierung von Typbibliotheken im System auf. Diese Aktion wird auf jede Datei angewendet, die in der TypeLib-Tabelle aufgelistet ist, die für die Deinstallation ausgelöst wird.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Unregistertypelibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352386"
---
# <a name="unregistertypelibraries-action"></a>Unregistertypelibraries-Aktion

Die unregistertypelibraries-Aktion hebt die Registrierung von Typbibliotheken im System auf. Diese Aktion wird auf jede Datei angewendet, die in der [typelib](typelib-table.md) -Tabelle aufgelistet ist, die für die Deinstallation ausgelöst wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die unregistertypelibraries-Aktion muss vor der [RemoveFiles](removefiles-action.md) -Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) einer nicht registrierten Typbibliothek. |



 

 

 



