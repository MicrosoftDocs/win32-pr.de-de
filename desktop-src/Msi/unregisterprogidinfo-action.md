---
description: Mit der unregisterprogidinfo-Aktion wird die Aufhebung der Registrierung von OLE ProgID-Informationen beim System verwaltet.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Unregisterprogidinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869036"
---
# <a name="unregisterprogidinfo-action"></a>Unregisterprogidinfo-Aktion

Mit der unregisterprogidinfo-Aktion wird die Aufhebung der Registrierung von OLE ProgID-Informationen beim System verwaltet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die unregisterprogidinfo-Aktion muss nach der Aktion [InstallInitialize](installinitialize-action.md) , [unregisterclassinfo](unregisterclassinfo-action.md) Action, [unregisterextensioninfo](unregisterextensioninfo-action.md) und vor der [registerprogidinfo](registerprogidinfo-action.md) -Aktion erfolgen.

[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterprogidinfo ' stehen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   Unregisterprogidinfo
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

Beispielsweise muss unregisterprogidinfo vor [unregistermimeinfo](unregistermimeinfo-action.md) in der Sequenz Tabelle stehen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                |
|-------|-------------------------------------------|
| \[1\] | Programm Bezeichner des registrierten Programms. |



 

## <a name="remarks"></a>Bemerkungen

Die unregisterprogidinfo-Aktion entfernt ProgID-Informationen aus der Registrierung ([ProgID-Tabelle](progid-table.md)) für Funktionen, die mit den Erweiterungs Informationen ([Erweiterungs Tabelle](extension-table.md)) oder den Klassen Informationen ([Klassen Tabelle](class-table.md)) verbunden sind und derzeit für die Deinstallation ausgewählt sind.

 

 



