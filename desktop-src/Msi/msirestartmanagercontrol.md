---
description: Die msirestartmanagercontrol-Eigenschaft gibt an, ob das Windows Installer Paket die Funktion Restart Manager oder FilesInUse verwendet.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Msirestartmanagercontrol (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359703"
---
# <a name="msirestartmanagercontrol-property"></a>Msirestartmanagercontrol (Eigenschaft)

Die **msirestartmanagercontrol** -Eigenschaft gibt an, ob das Windows Installer Paket die Funktion [Restart Manager](../rstmgr/restart-manager-portal.md) oder [FilesInUse](filesinuse-dialog.md) verwendet.

## <a name="value"></a>Wert



| Wert                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Dies ist der Standardwert, wenn die-Eigenschaft nicht festgelegt ist. Windows Installer versucht immer, den [Neustart-Manager](../rstmgr/restart-manager-portal.md) unter Windows Vista zu verwenden.<br/>                                                                                                                                                                                                       |
| <dl> <dt>Ier</dt> </dl>         | Deaktiviert die Interaktion des Pakets mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md). Windows Installer verwendet das [FilesInUse-Dialog](filesinuse-dialog.md)Feld. <br/>                                                                                                                                                                                                      |
| <dl> <dt>"Disableshutdown"</dt> </dl> | Windows Installer verwendet das [FilesInUse-Dialog](filesinuse-dialog.md)Feld. Mit dieser Einstellung werden Versuche durch den [Neustart-Manager](../rstmgr/restart-manager-portal.md) deaktiviert, um beim Installieren eines Windows Installer Pakets, das noch nicht für die Verwendung des Neustart-Managers erstellt wurde, Neustarts zu vermeiden. Der Installer verwendet weiterhin den Neustart-Manager, um die von Anwendungen verwendeten Dateien zu erkennen. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **msirestartmanagercontrol** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.

Der Wert dieser Eigenschaft kann mithilfe von Anpassungs Transformationen oder Upgrades geändert werden. Das Ändern des Werts dieser Eigenschaft von benutzerdefinierten Aktionen hat keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
