---
description: Die MsiNetAssemblySupport-Eigenschaft gibt an, ob der Computer Common Language-Laufzeitassemblys unterstützt.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d135fcc9eb301d3624586318fdc0d5dbbc534c5771ee89d4ae625af78b0782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944903"
---
# <a name="msinetassemblysupport-property"></a>MsiNetAssemblySupport(Eigenschaft)

Die **MsiNetAssemblySupport-Eigenschaft** gibt an, ob der Computer Common Language-Laufzeitassemblys unterstützt. Auf Systemen, die Common Language Run-Time-Assemblys unterstützen, legt das Installationsprogramm den Wert von **MsiNetAssemblySupport** auf die Dateiversion von Fusion.dll. Das Installationsprogramm setzt diese Eigenschaft nicht, wenn das Betriebssystem keine Common Language-Laufzeitassemblys unterstützt. Wenn mehrere Versionen von Fusion.dll auf dem Computer des Benutzers nebeneinander installiert werden, wird diese Eigenschaft auf die neueste Version der Fusion.dll festgelegt. Wenn beispielsweise .NET Framework Version 1.0.3705 (Fusion.dll Version 1.0.3705.15) und .NET Framework Version 1.1.4322 (Fusion.dll Version 1.1.4322.314) nebeneinander installiert sind, Die **MsiNetAssemblySupport-Eigenschaft** ist auf 1.1.4322.314 festgelegt. Weitere Informationen finden Sie unter [Assemblys](assemblies.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




