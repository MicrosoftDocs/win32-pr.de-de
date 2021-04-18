---
description: Die Stop Services-Aktion beendet Systemdienste. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Stop Services-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347253"
---
# <a name="stopservices-action"></a>Stop Services-Aktion

Die Stop Services-Aktion beendet Systemdienste. Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:

-   Stop Services
-   [Delta Service Services](deleteservices-action.md)

Eine der folgenden Aktionen:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [Duplicatefiles](duplicatefiles-action.md)
-   ["Muvefiles"](movefiles-action.md)
-   [Patchdateien](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [Installdienste](installservices-action.md)
-   [Startdienste](startservices-action.md)

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Dienst Anzeige Name.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Bemerkungen

Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Steuern von Diensten oder der Anwendung zu einer verwalteten Installation verfügt.

 

 



