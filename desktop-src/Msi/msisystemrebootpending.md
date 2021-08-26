---
description: Das Installationsprogramm legt den Wert der MsiSystemRebootPending-Eigenschaft auf 1 fest, wenn ein Vorgang zum Umbenennen einer Datei aussteht.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: MsiSystemRebootPending-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cab600ca7c0f1bbc240f8fb1a9d93f3da62914e8250863333b75f8973d6c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042650"
---
# <a name="msisystemrebootpending-property"></a>MsiSystemRebootPending-Eigenschaft

Das Installationsprogramm legt den Wert der **MsiSystemRebootPending-Eigenschaft** auf 1 fest, wenn ein Vorgang zum Umbenennen einer Datei aussteht.

Paketautoren können eine Bedingung in der [LaunchCondition-Tabelle](launchcondition-table.md) auf dieser Eigenschaft basieren, um die Installation ihres Pakets in Fällen zu verhindern, in denen ein Vorgang zum Umbenennen einer Datei aussteht. Dies kann geschehen, um einen Neustart des Betriebssystems zu verhindern, der durch die Umbenennung der Datei verursacht wird. Das Installationsprogramm legt die **MsiSystemRebootPending-Eigenschaft** nicht in allen Fällen fest, die einen Neustart des Systems erfordern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Systemneustarts](system-reboots.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




