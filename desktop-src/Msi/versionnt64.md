---
description: Das Installationsprogramm legt die VersionNT64-Eigenschaft nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262072"
---
# <a name="versionnt64-property"></a>VersionNT64-Eigenschaft

Das Installationsprogramm legt die **VersionNT64-Eigenschaft** nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird. Die -Eigenschaft ist nicht definiert, wenn das Betriebssystem nicht 64-Bit ist.

Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.

Aus Kompatibilitätsgründen ist die -Eigenschaft auch nicht definiert, wenn die [**Template Summary-Eigenschaft**](template-summary.md) angibt, dass das Paket für 32-Bit-Intel-Systeme (x86) gilt und das Betriebssystem keinen 64-Bit-Intel-Code (x64) ausführen kann, z. B. Windows 10 auf ARM (ARM64).

> [!NOTE]
> Ab Windows 10 Build 21277 verfügen ARM64-Builds im Dev-Kanal des Windows Insider Preview Programms über Unterstützung für x64-Anwendungen. Bei diesen ARM64-Builds wird die VersionNT64-Eigenschaft für x86-Pakete definiert.

## <a name="remarks"></a>Bemerkungen

Bedingte Ausdrücke testen für 64-Bit-Windows einfach mithilfe des Eigenschaftennamens oder durch Überprüfen der Version mithilfe eines Vergleichsoperators.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP finden Sie unter [Windows Installer Run-Time Requirements (Anforderungen für Windows Installer Run-Time)](windows-installer-portal.md) Informationen zum windows-Mindestdienstpaket, das für eine Windows Installer Version erforderlich ist.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




