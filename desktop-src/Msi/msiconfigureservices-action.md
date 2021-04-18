---
description: Die msikonfigurireservices-Aktion konfiguriert einen Dienst für das System. Mit dieser Aktion werden die Tabellen "msiserviceconfig" und "msiserviceconfigfailureactions" abgefragt.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Msikonfigurireservices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354872"
---
# <a name="msiconfigureservices-action"></a>Msikonfigurireservices-Aktion

Die msikonfigurireservices-Aktion konfiguriert einen Dienst für das System. Mit dieser Aktion werden die Tabellen " [msiserviceconfig](msiserviceconfig-table.md) " und " [msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md) " abgefragt.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Aktion ist ab Windows Installer 5,0 verfügbar.

> [!IMPORTANT]
>
> Windows-Dienste bieten die Möglichkeit, vordefinierte Aktionen als Reaktion auf einen Fehler in einem Dienst automatisch auszuführen. Um die programmgesteuerte Einrichtung dieser **Wiederherstellungs Aktionen** zu unterstützen, wenn ein Dienst fehlschlägt, wurde [msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md) der MSI in Version MSI 5,0 hinzugefügt. Diese Funktionalität funktioniert jedoch nicht wie erwartet.
>
> Um dieses Problem zu umgehen, sollte ein Anwendungsentwickler die **benutzerdefinierte Aktions** Funktionalität in msi verwenden, um **sc.exe** auszuführen und die **Wiederherstellungsoptionen** entsprechend festzulegen.

 

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Diese Standardaktion muss in der folgenden Reihenfolge verwendet werden.

[Stop Services](stopservices-action.md)

[Delta Service Services](deleteservices-action.md)

Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".

[Installdienste](installservices-action.md)

Msikonfigurireservices

[Startdienste](startservices-action.md)

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Für diese Aktion ist es erforderlich, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Installieren von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



