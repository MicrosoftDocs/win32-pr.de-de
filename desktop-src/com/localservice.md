---
title: LocalService
description: Installiert ein-Objekt als Dienst Anwendung.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Registrierungs Wert für LocalService (com)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858505"
---
# <a name="localservice"></a>LocalService

Installiert ein-Objekt als Dienst Anwendung.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Bemerkungen

Zusätzlich zur Ausführung als ausführbare Datei des lokalen Servers (exe) kann ein COM-Objekt sich auch für die Ausführung als Dienst Anwendung Verpacken, wenn es von einem lokalen oder Remote Client aktiviert wird. -Dienste unterstützen zahlreiche nützliche und Benutzeroberflächen integrierte Verwaltungsfunktionen, einschließlich lokaler und Remote Starts, beenden, anhalten und Neustarts, sowie die Möglichkeit, den Server für die Ausführung unter einem bestimmten Benutzerkonto und einer Fenster Station einzurichten.

Ein Objekt, das als Dienst geschrieben wird, wird für die Verwendung durch com installiert, indem ein **LocalService** -Wert eingerichtet und eine Standard Dienst Installation durchgeführt wird. Der Wert für **LocalService** muss auf den Dienstnamen festgelegt werden, der im **lokalen HKEY- \_ \_ \\ System \\ CurrentControlSet \\ Services** als Standard- **reg \_ SZ** -Wert konfiguriert ist.

Wenn " **LocalService** " festgelegt ist, wird jede Zeichenfolge, die [**Service Parameters**](serviceparameters.md) zugewiesen ist, beim Starten als Befehlszeilenargument an den Dienst übermittelt.

Die Dienst Konfiguration wird in vielen Situationen bevorzugt, in denen die Funktionen der lokalen und Remote-Dienstverwaltungs-APIs und die Benutzeroberfläche für die Dienste nützlich sein können, die das Objekt bereitstellt. Beispielsweise sollte die Verwendung des vorhandenen administrativen Frameworks der Dienst Architektur eine offensichtliche Wahl sein, wenn es sich um ein langlebiges Objekt handelt, oder es werden problemlos Konzepte wie das starten, beenden, zurücksetzen oder anhalten unterstützt.

Dienste können dynamisch konfiguriert werden, und Sie können so konfiguriert werden, dass Sie automatisch ausgeführt werden, wenn der Computer gestartet wird oder wenn Sie von einer Client Anwendung angefordert werden.

Wenn Sie Klassen als Dienste implementieren, sollten Sie die folgenden Punkte beachten:

-   Dieser Wert wird im Gegensatz zum [**LocalServer32**](localserver32.md) -Schlüssel für lokale und Remote Aktivierungs Anforderungen verwendet, wenn " **LocalService** " vorhanden ist und sich auf einen gültigen Dienst bezieht, wird die **LocalServer32** -Taste ignoriert.
-   Zurzeit kann nur eine einzelne Instanz einer Dienst Anwendung zu einem bestimmten Zeitpunkt auf einem Computer ausgeführt werden. COM-Dienste müssen daher Ihre Klassen Objekte beim Start mithilfe von REGCLS \_ multipleuse registrieren, um mehrere Clients zu unterstützen.
-   Um ordnungsgemäß zu starten und zu initialisieren, müssen COM-Dienste, die für die automatische Ausführung beim Starten eines Computers konfiguriert sind, RPCSS in der Liste der abhängigen Dienste enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[**Service Parameters**](serviceparameters.md)
</dt> <dt>

[Dienste](/windows/desktop/Services/services)
</dt> </dl>

 

 