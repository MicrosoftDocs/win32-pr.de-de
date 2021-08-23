---
description: Das Installationsprogramm legt den Wert der MsiPatchRemovalList-Eigenschaft auf eine Liste von Patches fest, die während der Installation entfernt werden.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: MsiPatchRemovalList(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93df2cdfc658875526c049ca7503e66a5c318df896a604a82c18751ac3358285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065980"
---
# <a name="msipatchremovallist-property"></a>MsiPatchRemovalList(Eigenschaft)

Das Installationsprogramm legt den Wert der **MsiPatchRemovalList-Eigenschaft** auf eine Liste von Patches fest, die während der Installation entfernt werden. Die Patches werden in der Liste durch ihre durch Semikolons getrennten Patchcode-GUIDs dargestellt.

Entwickler können die **MsiPatchRemovalList-Eigenschaft** verwenden, um ein Windows [](custom-actions.md) Installer-Paket oder einen Patch zu erstellen, das benutzerdefinierte Aktionen zum Entfernen eines Patches ausführt. Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch erstellt werden, der kein deinstallationsfähiger [Patch ist.](uninstallable-patches.md) Die benutzerdefinierte Aktion kann für die **MsiPatchRemovalList-Eigenschaft** in den Sequenztabellen bedingt werden. Weitere [Informationen zum Bedingten Festlegen](using-properties-in-conditional-statements.md) von Aktionen finden Sie unter Verwenden von Eigenschaften in bedingten Anweisungen.

Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der **MsiPatchRemovalList-Eigenschaft entfernt** werden. Die benutzerdefinierte Aktion kann bestimmen, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**MsiGetPatchInfoEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) oder die [**PatchProperty-Eigenschaft**](patch-patchproperty.md) des [Patch-Objekts aufruft.](patch-object.md)

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Entfernen von Patches finden Sie unter [Entfernen von Patches.](removing-patches.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




