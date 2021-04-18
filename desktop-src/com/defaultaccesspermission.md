---
title: DefaultAccessPermission
description: Legt die Access Control Liste (ACL) der Prinzipale fest, die auf Klassen zugreifen können, für die keine AccessPermission-Einstellung vorhanden ist.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- DefaultAccessPermission-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339184"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Legt die Access Control Liste (ACL) der Prinzipale fest, die auf Klassen zugreifen können, für die keine [**AccessPermission**](accesspermission.md) -Einstellung vorhanden ist. Diese ACL wird nur von Anwendungen verwendet, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und keinen **AccessPermission** -Wert unter Ihrem [**AppID**](appid-key.md) -Schlüssel haben.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** .

Die com-Laufzeit im Server überprüft die durch diesen Wert beschriebene ACL während der Identität des Aufrufers, der versucht, eine Verbindung mit dem Objekt herzustellen, und der Erfolg bestimmt, ob der Zugriff zugelassen oder nicht zulässig ist. Wenn die Zugriffs Überprüfung fehlschlägt, ist die Verbindung mit dem Objekt nicht zulässig. Wenn dieser benannte Wert nicht vorhanden ist, dürfen nur der Server Prinzipal und das lokale System den Server anrufen.

Standardmäßig enthält dieser Wert keine Einträge. Nur der Server Prinzipal und das System dürfen den Server anrufen.

Dieser Wert bietet eine einfache Ebene der zentralisierten Verwaltung des Standard Verbindungs Zugriffs auf die Ausführung von Objekten auf einem Computer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Access spermission**](accesspermission.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




