---
title: MachineLaunchRestriction
description: Legt die computerweite Einschränkungsrichtlinie für den Komponentenstart und die Aktivierung fest.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- MachineLaunchRestriction-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048058"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Legt die computerweite Einschränkungsrichtlinie für den Komponentenstart und die Aktivierung fest.

> [!Caution]  
> Das Ändern dieses Werts wirkt sich auf alle COM-Serveranwendungen aus und verhindert möglicherweise, dass sie ordnungsgemäß funktionieren. Wenn ES COM-Serveranwendungen gibt, die weniger strenge Einschränkungen als die computerweiten Einschränkungen aufweisen, kann die Reduzierung der computerweiten Einschränkungen diese Anwendungen möglicherweise für unerwünschten Zugriff verfügbar machen. Wenn Sie dagegen die computerweiten Einschränkungen erhöhen, kann auf einige COM-Serveranwendungen möglicherweise nicht mehr durch Aufrufen von Anwendungen zugegriffen werden.

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ BINARY-Wert.**

Prinzipale, denen hier keine Berechtigungen erteilt wurden, können sie auch dann nicht abrufen, wenn die Berechtigungen durch den [Registrierungswert DefaultAccessPermission](defaultaccesspermission.md) oder die [**CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) gewährt werden.

Standardmäßig können Administratoren lokale und Remotestart- und Aktivierungsberechtigungen erhalten, und Mitglieder der Gruppe Jeder können lokale Aktivierungs- und Startberechtigungen erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




