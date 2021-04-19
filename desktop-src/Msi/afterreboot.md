---
description: Der Installer legt die afterreboot-Eigenschaft nach einem von der ForceReboot-Aktion aufgerufenen Neustart auf 1 fest. Der Installer fügt afterreboot = 1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Afterreboot (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370282"
---
# <a name="afterreboot-property"></a>Afterreboot (Eigenschaft)

Der Installer legt die **afterreboot** -Eigenschaft nach einem von der [ForceReboot-Aktion](forcereboot-action.md)aufgerufenen Neustart auf 1 fest. Der Installer fügt afterreboot = 1 der Befehlszeile hinzu, die unmittelbar nach dem Neustart ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Die [ForceReboot-Aktion](forcereboot-action.md) muss immer mit einer Bedingungs Anweisung verwendet werden, damit das Installationsprogramm nur bei Bedarf einen Neustart auslöst. Möglicherweise ist ein Neustart erforderlich, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert wurde. Der Fall unterscheidet sich für jedes Produkt, und eine benutzerdefinierte Aktion ist möglicherweise erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist. Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die Eigenschaft **afterreboot** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[System Neustarts](system-reboots.md)
</dt> </dl>

 

 




