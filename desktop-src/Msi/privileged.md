---
description: Die Privileged-Eigenschaft gibt an, ob die Installation im Kontext von erhöhten Rechten ausgeführt wird.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privilegierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe61f17e5ef3453021c98bac8eb383171a678adfb204886ecdaa840e0df832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129130"
---
# <a name="privileged-property"></a>Privilegierte Eigenschaft

Die **Privileged-Eigenschaft** gibt an, ob die Installation im Kontext von erhöhten Rechten ausgeführt wird. Das Installationsprogramm legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt, die Anwendung von einem Systemadministrator zugewiesen wurde oder wenn die Benutzer- und Computerrichtlinien AlwaysInstallElevated auf TRUE festgelegt sind.

## <a name="default-value"></a>Standardwert

Das Installationsprogramm setzt diese Eigenschaft nicht, wenn der Benutzer nicht mit erhöhten Rechten installieren darf.

## <a name="remarks"></a>Hinweise

Entwickler von Installerpaketen können die **Privileged-Eigenschaft** verwenden, um die Installation von der Systemrichtlinie, dem Benutzer als Administrator oder der Zuweisung durch einen Administrator abhängig zu machen.

Bei der Ausführung auf Windows Vista sind **Privileged** und [**AdminUser**](adminuser.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




