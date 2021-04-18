---
description: Das Installationsprogramm legt den Wert der msirestartmanagersessionkey-Eigenschaft auf den Sitzungsschlüssel für die Restart Manager-Sitzung fest.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Msirestartmanagersessionkey (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365567"
---
# <a name="msirestartmanagersessionkey-property"></a>Msirestartmanagersessionkey (Eigenschaft)

Das Installationsprogramm legt den Wert der **msirestartmanagersessionkey** -Eigenschaft auf den Sitzungsschlüssel für die [Restart Manager](../rstmgr/restart-manager-portal.md) -Sitzung fest. Benutzerdefinierte Aktionen können den Sitzungsschlüssel verwenden, um der Sitzung für den [Neustart-Manager](../rstmgr/restart-manager-portal.md) beizutreten.

## <a name="remarks"></a>Bemerkungen

Der Installer legt den Wert der Eigenschaft " **msirestartmanagersessionkey** " bei der Initialisierung fest und löscht dann den Wert während der [InstallValidate](installvalidate-action.md) -Aktion. Benutzerdefinierte Aktionen, für die der Wert der **msirestartmanagersessionkey** -Eigenschaft erforderlich ist, müssen vor der InstallValidate-Aktion in der Aktions Sequenz liegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
