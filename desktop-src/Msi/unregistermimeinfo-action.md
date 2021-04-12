---
description: Die unregistermimeinfo-Aktion hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf. Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der MIME-Tabelle auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Unregistermimeinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218673"
---
# <a name="unregistermimeinfo-action"></a>Unregistermimeinfo-Aktion

Die unregistermimeinfo-Aktion hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf. Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der [MIME-Tabelle](mime-table.md) auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die unregistermimeinfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion, [unregisterclassinfo](unregisterclassinfo-action.md) Action, [unregisterextensioninfo](unregisterextensioninfo-action.md) Action und vor der [registermimeinfo](registermimeinfo-action.md) -Aktion erfolgen.

[Removeregistryvalues](removeregistryvalues-action.md) muss vor unregistermimeinfo in der Sequenz stehen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   Unregistermimeinfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

Beispielsweise muss unregistermimeinfo in der Sequenz Tabelle vor [RegisterExtensionInfo](registerextensioninfo-action.md) stehen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                    |
|-------|-----------------------------------------------|
| \[1\] | Der Bezeichner des nicht registrierten MIME-Inhaltstyps. |
| \[2\] | Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist.  |



 

 

 



