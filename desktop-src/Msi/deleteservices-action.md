---
description: Mit der Aktion "Delta Service" wird ein Dienst angehalten, und die Registrierung wird aus dem System entfernt. Durch diese Aktion wird die ServiceControl-Tabelle abgefragt.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Delta Service-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346348"
---
# <a name="deleteservices-action"></a>Delta Service-Aktion

Mit der Aktion "Delta Service" wird ein Dienst angehalten, und die Registrierung wird aus dem System entfernt. Durch diese Aktion wird die [ServiceControl-Tabelle](servicecontrol-table.md)abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Dienst Aktionen müssen in der folgenden Reihenfolge verwendet werden:

1.  [Stop Services](stopservices-action.md)
2.  Delta Service Services
3.  Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".
4.  [Installservices-Aktion](installservices-action.md)
5.  [Startdienste](startservices-action.md)

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Dienst Anzeige Name.      |
| \[2\] | Dienstname              |



 

## <a name="remarks"></a>Bemerkungen

Diese Aktion erfordert, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Löschen von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



