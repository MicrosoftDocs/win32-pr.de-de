---
description: Mit der Aktion StartServices werden Systemdienste gestartet. Diese Aktion fragt die ServiceControl-Tabelle ab.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: StartServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ff7b927eb4bc157530cebe9767ef7a434d92f0b72f9e6c799b02a2969f5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627530"
---
# <a name="startservices-action"></a>StartServices-Aktion

Mit der Aktion StartServices werden Systemdienste gestartet. Diese Aktion fragt die [ServiceControl-Tabelle](servicecontrol-table.md)ab.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Dienstaktionen müssen in der folgenden Reihenfolge verwendet werden:

-   [StopServices](stopservices-action.md)
-   [DeleteServices](deleteservices-action.md)

Eine der folgenden Aktionen:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   StartServices

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Anzeigename des Diensts.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Hinweise

Diese Aktion erfordert, dass der Benutzer Administrator ist oder über erhöhte Berechtigungen mit der Berechtigung zum Steuern von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



