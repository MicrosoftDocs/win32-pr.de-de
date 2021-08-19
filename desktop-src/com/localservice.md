---
title: LocalService
description: Installiert ein Objekt als Dienstanwendung.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- LocalService-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e454566ac505907f66fad585062bc67f41c865df45b30405b83e5faadef7f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736466"
---
# <a name="localservice"></a>LocalService

Installiert ein Objekt als Dienstanwendung.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Hinweise

Zusätzlich zur Ausführung als lokale ausführbare Serverdatei (EXE) kann sich ein COM-Objekt auch selbst packen, um als Dienstanwendung ausgeführt zu werden, wenn es von einem lokalen oder Remoteclient aktiviert wird. Dienste unterstützen zahlreiche nützliche und in die Benutzeroberfläche integrierte Verwaltungsfeatures, z. B. lokales Starten und Remotestarten, Beenden, Anhalten und Neustarten sowie die Möglichkeit, den Server für die Ausführung unter einem bestimmten Benutzerkonto und einer bestimmten Fensterstation zu erstellen.

Ein als Dienst geschriebenes Objekt wird für die Verwendung durch COM installiert, indem ein **LocalService-Wert** erstellt und eine Standarddienstinstallation ausgeführt wird. Der **LocalService-Wert** muss auf den Dienstnamen festgelegt werden, wie in **HKEY \_ LOCAL MACHINE \_ \\ System \\ CurrentControlSet \\ Services** konfiguriert, als **Standard-REG \_ SZ-Wert.**

Wenn **LocalService** festgelegt ist, wird jede Zeichenfolge, die [**ServiceParameters**](serviceparameters.md) zugewiesen ist, beim Start als Befehlszeilenargument an den Dienst übergeben.

Die Dienstkonfiguration wird in vielen Situationen bevorzugt, in denen die Funktionen der lokalen und Remotedienstverwaltungs-APIs und der Benutzeroberfläche für die dienste nützlich sein können, die das -Objekt bietet. Beispielsweise sollte die Nutzung des vorhandenen administrativen Frameworks der Dienstarchitektur eine offensichtliche Wahl sein, wenn das Objekt langlebig ist oder Konzepte wie das Starten, Beenden, Zurücksetzen oder Anhalten unterstützt.

Dienste können dynamisch konfiguriert und so konfiguriert werden, dass sie automatisch ausgeführt werden, wenn der Computer gestartet wird, oder dass sie gestartet werden, wenn sie von einer Clientanwendung angefordert werden.

Wenn Sie Klassen als Dienste implementieren, sollten Sie die folgenden Punkte beachten:

-   Dieser Wert wird für lokale und Remoteaktivierungsanforderungen gegenüber dem [**LocalServer32-Schlüssel**](localserver32.md) verwendet. Wenn **LocalService** vorhanden ist und auf einen gültigen Dienst verweist, wird der **LocalServer32-Schlüssel** ignoriert.
-   Derzeit kann nur eine einzelne Instanz einer Dienstanwendung zu einem bestimmten Zeitpunkt auf einem Computer ausgeführt werden. COM-Dienste müssen daher ihre Klassenobjekte beim Start mithilfe von REGCLS \_ MULTIPLEUSE registrieren, um mehrere Clients zu unterstützen.
-   Um ordnungsgemäß zu starten und zu initialisieren, müssen COM-Dienste, die für die automatische Ausführung beim Starten eines Computers konfiguriert sind, RPCSS in der Liste der abhängigen Dienste enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Dienste](/windows/desktop/Services/services)
</dt> </dl>

 

 