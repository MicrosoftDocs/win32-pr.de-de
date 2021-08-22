---
description: Das Installationsprogramm legt die VersionNT64-Eigenschaft nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285f97a6325df65ace9ff6620489697e6eeeb573761437bd0a826dec4dc31e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526930"
---
# <a name="versionnt64-property"></a>VersionNT64 (Eigenschaft)

Das Installationsprogramm legt die **VersionNT64-Eigenschaft** nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird. Die -Eigenschaft ist nicht definiert, wenn das Betriebssystem nicht 64-Bit ist.

Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.

Aus Kompatibilitätsgründen ist die Eigenschaft auch [](template-summary.md) nicht definiert, wenn die Eigenschaft Vorlagenzusammenfassung angibt, dass das Paket für 32-Bit-Intel-Systeme (x86) gilt und das Betriebssystem keinen 64-Bit-Intel (x64)-Code ausführen kann, z. B. Windows 10 auf ARM (ARM64).

> [!NOTE]
> Ab Windows 10 Build 21277 unterstützen ARM64-Builds im Dev-Kanal des Windows Insider Preview-Programms x64-Anwendungen. Bei diesen ARM64-Builds wird die VersionNT64-Eigenschaft für x86-Pakete definiert.

## <a name="remarks"></a>Hinweise

Bedingte Ausdrücke testen auf 64-Bit-Windows einfach mithilfe des Eigenschaftennamens oder durch Überprüfen der Version mithilfe eines Vergleichsoperator.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Das Installationsprogramm auf Windows Server 2003 oder Windows XP finden Sie unter [Windows Installer Run-Time Requirements](windows-installer-portal.md) (Run-Time-Anforderungen für Windows Service Pack), das für eine Windows Installer-Version erforderlich ist.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




