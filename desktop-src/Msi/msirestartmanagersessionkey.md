---
description: Das Installationsprogramm legt den Wert der MsiRestartManagerSessionKey-Eigenschaft auf den Sitzungsschlüssel für die Restart Manager-Sitzung fest.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: MsiRestartManagerSessionKey-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f48fe8d2ce4b287afc5c222acdc1f71eec393ff9a1ab1773a822e30405e6a317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944538"
---
# <a name="msirestartmanagersessionkey-property"></a>MsiRestartManagerSessionKey-Eigenschaft

Das Installationsprogramm legt den Wert der **MsiRestartManagerSessionKey-Eigenschaft** auf den Sitzungsschlüssel für die [Restart Manager-Sitzung](../rstmgr/restart-manager-portal.md) fest. Benutzerdefinierte Aktionen können den Sitzungsschlüssel verwenden, um der [Neustart-Manager-Sitzung](../rstmgr/restart-manager-portal.md) beizutreten.

## <a name="remarks"></a>Hinweise

Das Installationsprogramm legt den Wert der **MsiRestartManagerSessionKey-Eigenschaft** bei der Initialisierung fest und löscht den Wert dann während der [InstallValidate-Aktion.](installvalidate-action.md) Benutzerdefinierte Aktionen, die den Wert der **MsiRestartManagerSessionKey-Eigenschaft** benötigen, müssen vor der InstallValidate-Aktion in der Aktionssequenz erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Informationen zum service pack-Mindestwert, der für eine Windows Installer-Version erforderlich ist, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
