---
description: Die Aktion StopServices beendet Systemdienste. Diese Aktion fragt die ServiceControl-Tabelle ab.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: StopServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627380"
---
# <a name="stopservices-action"></a>StopServices-Aktion

Die Aktion StopServices beendet Systemdienste. Diese Aktion fragt die [ServiceControl-Tabelle ab.](servicecontrol-table.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Dienstaktionen müssen in der folgenden Reihenfolge verwendet werden:

-   StopServices
-   [DeleteServices](deleteservices-action.md)

Eine der folgenden Aktionen:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Anzeigename des Diensts.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Hinweise

Diese Aktion erfordert, dass der Benutzer Administrator ist oder über erhöhte Berechtigungen mit der Berechtigung zum Steuern von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



