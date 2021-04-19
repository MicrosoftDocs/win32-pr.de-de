---
description: Mit der Eigenschaft "privilegiert" wird angegeben, ob die Installation im Kontext erhöhter Berechtigungen erfolgt.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privilegierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370332"
---
# <a name="privileged-property"></a>Privilegierte Eigenschaft

Mit der Eigenschaft " **privilegiert** " wird angegeben, ob die Installation im Kontext erhöhter Berechtigungen erfolgt. Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt, wenn die Anwendung von einem Systemadministrator zugewiesen wurde, oder wenn die Benutzer-und Computer Richtlinien alwaysinstallerhöhten auf true festgelegt sind.

## <a name="default-value"></a>Standardwert

Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn der Benutzer nicht mit erhöhten Rechten installieren darf.

## <a name="remarks"></a>Bemerkungen

Entwickler von Installer-Paketen können mithilfe der Eigenschaft **privilegiert** die Installation abhängig von der System Richtlinie, dem Benutzer, der Administrator ist, oder der Zuweisung durch einen Administrator machen.

Bei der Ausführung unter Windows Vista sind die Berechtigungen " **privilegiert** " und " [**AdminUser**](adminuser.md) " identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




