---
description: Mit der Option zum Deinstallieren von benutzerdefinierten Aktionen können Sie angeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann ausführen soll, wenn ein Patch deinstalliert wird.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Patch zum Deinstallieren benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340187"
---
# <a name="patch-uninstall-custom-actions"></a>Patch zum Deinstallieren benutzerdefinierter Aktionen

Mit der Option zum [Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) können Sie angeben, dass das Installationsprogramm die benutzerdefinierte Aktion nur dann ausführen soll, wenn ein Patch deinstalliert wird.

**Windows Installer 4,5 und höher:** Sie können die [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) verwenden, um anzugeben, dass das Installationsprogramm nur die benutzerdefinierte Aktion ausführen soll, wenn ein Patch deinstalliert wird.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md): * *

Die [Option zum Deinstallieren des benutzerdefinierten Aktions Patches](custom-action-patch-uninstall-option.md) ist nicht verfügbar. Es gibt keine Möglichkeit, eine [benutzerdefinierte Aktion](custom-actions.md) innerhalb eines Patchpakets zu markieren, die ausgeführt wird, wenn der Patch deinstalliert wird, da das Installationsprogramm nicht die zu installierenden Patchpakete anwendet.

Um eine [benutzerdefinierte Aktion](custom-actions.md) auszuführen, wenn ein bestimmter Patch deinstalliert wird, muss die benutzerdefinierte Aktion entweder in der ursprünglichen Anwendung vorhanden sein oder sich in einem Patch für das Produkt befinden, das immer angewendet wird.

Entwickler können die [**msipatchremovallist**](msipatchremovallist.md) -Eigenschaft verwenden, um ein Windows Installer Paket oder einen Patch zu erstellen, der beim Entfernen eines Patches [benutzerdefinierte Aktionen](custom-actions.md) ausführt. Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch, bei dem es sich nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt, erstellt werden. Die benutzerdefinierte Aktion kann für die **msipatchremovallist** -Eigenschaft in den Sequenz Tabellen conditionalisiert werden. Weitere Informationen zu conditionalisierungsaktionen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md) .

Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der [**msipatchremovallist**](msipatchremovallist.md) -Eigenschaft entfernt werden. Die benutzerdefinierte Aktion kann ermitteln, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Eigenschaft oder die [**patchproperty**](patch-patchproperty.md) -Eigenschaft des [Patch-Objekts](patch-object.md)aufgerufen wird.

Wenn für die benutzerdefinierte Aktion besondere Metadaten aus dem Patch erforderlich sind, sollte der Patch eine benutzerdefinierte Aktion enthalten, die die Metadaten in einen Registrierungs-oder Datei Speicherort schreibt, wenn der Patch angewendet wird. Die benutzerdefinierte Aktion in der ursprünglichen Anwendung oder ein Patch, das immer angewendet wird, kann die zum Entfernen der Änderungen des Patches benötigten Informationen abrufen.

Patches, die Änderungen vornehmen, die nur schwer rückgängig gemacht werden können, sollten nicht als [nicht installierbare Patches](uninstallable-patches.md)gekennzeichnet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Entfernen von Patches](removing-patches.md)
</dt> <dt>

[Nicht installierbare Patches](uninstallable-patches.md)
</dt> <dt>

[Patches werden deinstalliert.](uninstalling-patches.md)
</dt> <dt>

[**Msipatchremove**](msipatchremove.md)
</dt> <dt>

[**Msienumapplicationsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



