---
description: Sie können die Option Custom Action Patch Uninstall verwenden, um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur ausführen soll, wenn ein Patch deinstalliert wird.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Benutzerdefinierte Aktionen zur Patchdeinstallation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69077337b80177984ff43f12038edb1daa48215f92c627f4ed22ea2f69c876b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145423"
---
# <a name="patch-uninstall-custom-actions"></a>Benutzerdefinierte Aktionen zur Patchdeinstallation

Sie können die Option [Custom Action Patch Uninstall verwenden,](custom-action-patch-uninstall-option.md) um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur ausführen soll, wenn ein Patch deinstalliert wird.

**Windows Installer 4.5 und höher:** Sie können die Deinstallationsoption [Benutzerdefinierte Aktionspatch verwenden,](custom-action-patch-uninstall-option.md) um anzugeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur ausführen soll, wenn ein Patch deinstalliert wird.

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)**

Die [Option "Patch deinstallieren" für benutzerdefinierte Aktionen](custom-action-patch-uninstall-option.md) ist nicht verfügbar. Es gibt keine Methode [](custom-actions.md) zum Markieren einer benutzerdefinierten Aktion innerhalb eines Patchpakets, die ausgeführt werden soll, wenn der Patch deinstalliert wird, da das Installationsprogramm die zu deinstallierenden Patchpakete nicht übernimmt.

Damit eine [benutzerdefinierte](custom-actions.md) Aktion ausgeführt wird, wenn ein bestimmter Patch deinstalliert wird, muss die benutzerdefinierte Aktion entweder in der ursprünglichen Anwendung oder in einem Patch für das Produkt vorhanden sein, das immer angewendet wird.

Entwickler können die [**MsiPatchRemovalList-Eigenschaft**](msipatchremovallist.md) verwenden, um ein Windows [](custom-actions.md) Installer-Paket oder einen Patch zu erstellen, das benutzerdefinierte Aktionen zum Entfernen eines Patches ausführt. Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch erstellt werden, der kein deinstallationsfähiger [Patch ist.](uninstallable-patches.md) Die benutzerdefinierte Aktion kann für die **MsiPatchRemovalList-Eigenschaft** in den Sequenztabellen bedingt werden. Weitere [Informationen zum Bedingten Festlegen](using-properties-in-conditional-statements.md) von Aktionen finden Sie unter Verwenden von Eigenschaften in bedingten Anweisungen.

Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der [**MsiPatchRemovalList-Eigenschaft entfernt**](msipatchremovallist.md) werden. Die benutzerdefinierte Aktion kann bestimmen, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem [**msiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) oder die [**PatchProperty-Eigenschaft**](patch-patchproperty.md) des [Patch-Objekts aufruft.](patch-object.md)

Wenn die benutzerdefinierte Aktion spezielle Metadaten aus dem Patch erfordert, sollte der Patch eine benutzerdefinierte Aktion enthalten, die die Metadaten in eine Registrierung oder einen Dateispeicherort schreibt, wenn der Patch angewendet wird. Die benutzerdefinierte Aktion in der ursprünglichen Anwendung oder ein Patch, der immer angewendet wird, kann die Informationen abrufen, die zum Entfernen der Patchänderungen erforderlich sind.

Patches, die Änderungen vornehmen, die schwer rückgängig gemacht werden können, sollten nicht als [deinstallationsfähige Patches markiert werden.](uninstallable-patches.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Entfernen von Patches](removing-patches.md)
</dt> <dt>

[Deinstallationsfähige Patches](uninstallable-patches.md)
</dt> <dt>

[Deinstallieren von Patches](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



