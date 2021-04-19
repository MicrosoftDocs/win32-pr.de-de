---
description: Die Start Services-Aktion startet Systemdienste. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: StartServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348309"
---
# <a name="startservices-action"></a>StartServices-Aktion

Die Start Services-Aktion startet Systemdienste. Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:

-   [Stop Services](stopservices-action.md)
-   [Delta Service Services](deleteservices-action.md)

Eine der folgenden Aktionen:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [Duplicatefiles](duplicatefiles-action.md)
-   ["Muvefiles"](movefiles-action.md)
-   [Patchdateien](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [Installdienste](installservices-action.md)
-   Startdienste

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Dienst Anzeige Name.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Bemerkungen

Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Steuern von Diensten oder der Anwendung zu einer verwalteten Installation verfügt.

 

 



