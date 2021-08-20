---
description: Die DeleteServices-Aktion beendet einen Dienst und entfernt seine Registrierung aus dem System. Diese Aktion fragt die ServiceControl-Tabelle ab.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: DeleteServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379116"
---
# <a name="deleteservices-action"></a>DeleteServices-Aktion

Die DeleteServices-Aktion beendet einen Dienst und entfernt seine Registrierung aus dem System. Diese Aktion fragt die [ServiceControl-Tabelle ab.](servicecontrol-table.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Dienstaktionen müssen in der folgenden Reihenfolge verwendet werden:

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  Eine der folgenden Aktionen: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)und [RemoveDuplicateFiles](removeduplicatefiles-action.md) Aktionen.
4.  [InstallServices-Aktion](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Anzeigename des Diensts.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Hinweise

Diese Aktion erfordert, dass der Benutzer Administrator ist oder über erhöhte Berechtigungen mit der Berechtigung zum Löschen von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



