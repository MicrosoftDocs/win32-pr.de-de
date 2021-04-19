---
description: Das Installationsprogramm legt den Wert der msipatchremovallist-Eigenschaft auf eine Liste von Patches fest, die während der Installation entfernt werden.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Msipatchremovallist (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354089"
---
# <a name="msipatchremovallist-property"></a>Msipatchremovallist (Eigenschaft)

Das Installationsprogramm legt den Wert der **msipatchremovallist** -Eigenschaft auf eine Liste von Patches fest, die während der Installation entfernt werden. Die Patches werden in der Liste durch die durch Semikolons getrennten patchcodeguids dargestellt.

Entwickler können die **msipatchremovallist** -Eigenschaft verwenden, um ein Windows Installer Paket oder einen Patch zu erstellen, der beim Entfernen eines Patches [benutzerdefinierte Aktionen](custom-actions.md) ausführt. Die benutzerdefinierte Aktion kann im ursprünglichen Installationspaket, einem Patch, der bereits auf das Paket angewendet wurde, oder einem Patch, bei dem es sich nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt, erstellt werden. Die benutzerdefinierte Aktion kann für die **msipatchremovallist** -Eigenschaft in den Sequenz Tabellen conditionalisiert werden. Weitere Informationen zu conditionalisierungsaktionen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md) .

Die benutzerdefinierte Aktion kann die GUIDs von Patches abrufen, die aus dem Wert der **msipatchremovallist** -Eigenschaft entfernt werden. Die benutzerdefinierte Aktion kann ermitteln, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Funktion oder die [**patchproperty**](patch-patchproperty.md) -Eigenschaft des [Patch-Objekts](patch-object.md)aufgerufen wird.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Entfernen von Patches finden Sie unter [Entfernen von Patches](removing-patches.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




