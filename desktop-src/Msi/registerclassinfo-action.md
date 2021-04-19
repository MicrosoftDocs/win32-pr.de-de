---
description: Mit der RegisterClassInfo-Aktion wird die Registrierung von COM-Klassen Informationen beim System verwaltet. Es verwendet die AppID-Tabelle.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: RegisterClassInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373028"
---
# <a name="registerclassinfo-action"></a>RegisterClassInfo-Aktion

Mit der RegisterClassInfo-Aktion wird die Registrierung von COM-Klassen Informationen beim System verwaltet. Es verwendet die [AppID-Tabelle](appid-table.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die RegisterClassInfo-Aktion muss nach der Aktion " [InstallFiles](installfiles-action.md) " und der Aktion " [unregisterclassinfo](unregisterclassinfo-action.md) " erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

So muss z. b. registerClassInfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                          |
|-------|-----------------------------------------------------|
| \[1\] | GUID-Klassen Bezeichner des registrierten COM-Servers. |



 

## <a name="remarks"></a>Bemerkungen

Wenn das System install-on-Demand für OLE-Server unterstützt, registriert RegisterClassInfo alle COM-Klassen in der [Klassen Tabelle](class-table.md) , die einer für die Installation oder Ankündigung ausgewählten Funktion zugeordnet sind. Andernfalls werden durch diese Aktion nur die com-Klassen registriert, die einer für die Installation ausgewählten Funktion zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Oleadvtsupport (Eigenschaft)**](oleadvtsupport.md)
</dt> </dl>

 

 



