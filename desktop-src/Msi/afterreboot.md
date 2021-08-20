---
description: Das Installationsprogramm legt die AFTERREBOOT-Eigenschaft nach einem Neustart, der von der ForceReboot-Aktion aufgerufen wurde, auf 1 fest. Das Installationsprogramm fügt AFTERREBOOT=1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: AFTERREBOOT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145913"
---
# <a name="afterreboot-property"></a>AFTERREBOOT-Eigenschaft

Das Installationsprogramm legt die **AFTERREBOOT-Eigenschaft** nach einem Neustart, der von der [ForceReboot-Aktion](forcereboot-action.md)aufgerufen wurde, auf 1 fest. Das Installationsprogramm fügt AFTERREBOOT=1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.

## <a name="remarks"></a>Hinweise

Die [ForceReboot-Aktion](forcereboot-action.md) muss immer mit einer bedingungsbedingten Anweisung verwendet werden, damit das Installationsprogramm nur bei Bedarf einen Neustart auslöst. Ein Neustart ist möglicherweise erforderlich, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert wurde. Der Fall ist für jedes Produkt unterschiedlich, und möglicherweise ist eine benutzerdefinierte Aktion erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist. Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die **AFTERREBOOT-Eigenschaft.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Systemneustarts](system-reboots.md)
</dt> </dl>

 

 




