---
title: DefaultLaunchPermission
description: Definiert die Access Control Liste (ACL) der Prinzipale, die Klassen starten können, die nicht Ihre eigene ACL über den Registrierungs Wert launchberechtigungstyp angeben.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Defaultlaunchberechtigungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342090"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Definiert die Access Control Liste (ACL) der Prinzipale, die Klassen starten können, die nicht Ihre eigene ACL über den Registrierungs Wert [**launchberechtigungstyp**](launchpermission.md) angeben.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** .

Die Standard Zugriffsberechtigungen lauten wie folgt:

-   Administratoren: Start zulassen
-   System: Start zulassen
-   Interaktiv: Start zulassen

Wenn der [**launchberechtigungswert**](launchpermission.md) für einen Server festgelegt ist, hat er Vorrang vor dem **defaultlaunchberechtigungswert** . Wenn eine lokale oder eine Remote Anforderung zum Starten eines Servers empfangen wird, dessen [**AppID**](appid-key.md) -Schlüssel keinen eigenen **launchberechtigungswert** hat, wird die durch diesen Wert beschriebene ACL während der Identität des Clients aktiviert, und Ihr Erfolg ermöglicht das Starten des Klassen Codes entweder oder nicht.

Dieser Wert stellt eine einfache Ebene der zentralisierten Verwaltung des standardmäßigen Zugriffs Zugriffs auf ansonsten nicht verwaltete Klassen auf einem Computer bereit. Ein Administrator kann z. b. das DCOMCNFG-Tool verwenden, um das System so zu konfigurieren, dass es den schreibgeschützten Zugriff für Poweruser zulässt. OLE schränkt daher Anforderungen zum Starten von Klassen Code für Mitglieder der Hauptbenutzer Gruppe ein. Ein Administrator kann anschließend Start Berechtigungen für einzelne Klassen konfigurieren, um die Möglichkeit zu erteilen, bei Bedarf Klassen Code für andere Gruppen oder einzelne Benutzer zu starten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Launchberechtigung**](launchpermission.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




