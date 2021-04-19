---
description: Der Installer legt den Wert der Eigenschaft msisystemrebootpending auf 1 fest, wenn ein Vorgang aussteht, um eine Datei umzubenennen.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Msisystemrebootpending (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367709"
---
# <a name="msisystemrebootpending-property"></a>Msisystemrebootpending (Eigenschaft)

Der Installer legt den Wert der Eigenschaft **msisystemrebootpending** auf 1 fest, wenn ein Vorgang aussteht, um eine Datei umzubenennen.

Paket Autoren können eine Bedingung in der [LaunchCondition-Tabelle](launchcondition-table.md) für diese Eigenschaft basieren, um die Installation des Pakets zu verhindern, wenn ein Vorgang aussteht, um eine Datei umzubenennen. Dies kann durchgeführt werden, um einen Neustart des Betriebssystems zu verhindern, das durch das Umbenennen der Datei verursacht wurde. Der Installer legt die **msisystemrebootpending** -Eigenschaft nicht in allen Fällen fest, für die ein Neustart des Systems erforderlich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[System Neustarts](system-reboots.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




