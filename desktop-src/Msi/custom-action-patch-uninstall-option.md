---
description: Verwenden Sie das folgende Optionsflag, um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann durchführt, wenn ein Patch deinstalliert wird. Fügen Sie den Wert in dieser Tabelle dem Wert im Feld "extendedtype" der Tabelle "CustomAction" hinzu, um die Option festzulegen.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Option zum Deinstallieren von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352587"
---
# <a name="custom-action-patch-uninstall-option"></a>Option zum Deinstallieren von benutzerdefinierten Aktionen

Verwenden Sie das folgende Optionsflag, um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann durchführt, wenn ein Patch deinstalliert wird. Fügen Sie den Wert in dieser Tabelle dem Wert im Feld "extendedtype" der [Tabelle "CustomAction](customaction-table.md)" hinzu, um die Option festzulegen.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Option ist ab Windows Installer 4,5 verfügbar.



| Konstante                                | Hexadezimal | Decimal | BESCHREIBUNG                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbcustomaktiontypepatchuninstall** | 0x8000      | 32768   | Die benutzerdefinierte Aktion wird nur ausgeführt, wenn ein Patch deinstalliert wird. |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann einer benutzerdefinierten Aktion hinzugefügt werden, indem es im Windows Installer Paket (MSI-Datei) gespeichert wird. Eine neue benutzerdefinierte Aktion mit diesem Attribut kann von einem Patch hinzugefügt werden. Eine benutzerdefinierte Aktion, in der dieses Attribut vorhanden ist, kann durch einen Patch aktualisiert werden. Dieses Attribut kann einer vorhandenen benutzerdefinierten Aktion nicht durch einen Patch hinzugefügt oder daraus entfernt werden.

Wenn ein Patch eine benutzerdefinierte Aktion mit diesem Attribut hinzufügt oder aktualisiert, Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion ausführt, wenn der Patch deinstalliert wird. Durch Windows Installer werden die Updates, die im Patch deinstalliert werden, für die benutzerdefinierte Aktion zum Deinstallieren von Patches verfügbar. Der Patch muss eine [msitransformview *<PatchGUID>*](msitransformview.md) -Tabelle enthalten, um diese Informationen für Windows Installer bereitzustellen.

Wenn ein Paket, das eine benutzerdefinierte Aktion mit dem **msidbcustomaction typepatchuninstall** -Attribut enthält, unter Verwendung einer Installerversion vor Windows Installer 4,0 installiert wird, ruft das Installationsprogramm die benutzerdefinierte Aktion nicht auf, wenn der Patch deinstalliert wird. Die Installation kann die benutzerdefinierte Aktion während der Installation, Reparatur oder Aktualisierung des Pakets ausführen.

Benutzerdefinierte Aktionen mit dem **msidbcustomaction typepatchuninstall** -Attribut sollten mithilfe der [**msipatchremove**](msipatchremove.md) -Eigenschaft bedingt werden, um zu verhindern, dass die benutzerdefinierte Aktion beim Installieren, reparieren oder aktualisieren mit einem System mit Windows Installer 4,0 oder früher ausgeführt wird. Wenn Windows Installer 4,5 und höher installiert ist, wird bei der Deinstallation des Patches für alle Patches auf dem System, die mit dem **msidbcustomaction typepatchuninstall** -Attribut gekennzeichnet sind, die benutzerdefinierte Aktion ausgeführt. Wenn Windows Installer 4,5 oder höher aus dem System entfernt wird, verlieren Patches die Funktion zum Deinstallieren von benutzerdefinierten Aktions Patches.

Informationen zum Ausführen einer benutzerdefinierten Aktion während der Deinstallation eines Patches mit einer früheren Version als Windows Installer 4,5 finden Sie unter [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
</dt> <dt>

[Msitransformview *<PatchGUID>*](msitransformview.md)
</dt> </dl>

 

 



