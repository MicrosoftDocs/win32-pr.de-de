---
description: Die MsiNetAssemblySupport-Eigenschaft gibt an, ob der Computer Common Language Run-Time-Assemblys unterstützt.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367639"
---
# <a name="msinetassemblysupport-property"></a>MsiNetAssemblySupport (Eigenschaft)

Die **MsiNetAssemblySupport** -Eigenschaft gibt an, ob der Computer Common Language Run-Time-Assemblys unterstützt. Auf Systemen, die Common Language Run-Time-Assemblys unterstützen, legt das Installationsprogramm den Wert von **MsiNetAssemblySupport** auf die Dateiversion von Fusion.dll fest. Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn das Betriebssystem keine Common Language Run-Time-Assemblys unterstützt. Wenn mehrere Versionen von Fusion.dll nebeneinander auf dem Computer des Benutzers installiert sind, wird diese Eigenschaft auf die neueste Version der Fusion.dll Datei festgelegt. Wenn z. b. .NET Framework Version 1.0.3705 (Fusion.dll Version 1.0.3705.15) und .NET Framework Version 1.1.4322 (Fusion.dll Version 1.1.4322.314) nebeneinander installiert sind, wird die Eigenschaft **MsiNetAssemblySupport** auf 1.1.4322.314 festgelegt. Weitere Informationen finden Sie unter [](assemblies.md)Assemblys.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




