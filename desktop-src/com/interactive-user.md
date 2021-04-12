---
title: Interaktiver Benutzer
description: Der interaktive Benutzer ist der Benutzer, der zurzeit an dem Computer angemeldet ist, auf dem der com-Server ausgeführt wird.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316520"
---
# <a name="interactive-user"></a>Interaktiver Benutzer

Der *interaktive Benutzer* ist der Benutzer, der zurzeit an dem Computer angemeldet ist, auf dem der com-Server ausgeführt wird. Wenn die Identität als interaktiver Benutzer festgelegt ist, verwenden alle Clients die gleiche Instanz des Servers, wenn der Server seine Klassenfactory als mehrfach verwendende Registrierung registriert. Wenn kein Benutzer angemeldet ist, wird der Server nicht ausgeführt. Wenn der Server über eine grafische Benutzeroberfläche (GUI) verfügt, die der Client sehen muss, sollten Sie den interaktiven Benutzer für die Identität des Servers verwenden. Das Auswählen dieser Identität birgt jedoch einige Sicherheitsrisiken, da der Server mit der Identität des angemeldeten Benutzers ausgeführt wird, ohne dass das wissen oder die Zustimmung des angemeldeten Benutzers erfolgt ist. Außerdem kann eine-Dienst Anwendung keine Benutzeroberfläche anzeigen. Weitere Informationen finden Sie unter [interaktive Dienste](/windows/desktop/Services/interactive-services).

Wenn ein com-Server so konfiguriert ist, dass er als interaktiver Benutzer ausgeführt wird, wird der Server in einer Terminaldiensteumgebung in der interaktiven Sitzung gestartet, die mit der Benutzeridentität des Clients übereinstimmt. Die Client Anwendung kann jedoch den sitzungsmoniker verwenden, um auf ein Objekt zu verweisen, das in einer Sitzung vom Server bereitgestellt wird, die nicht mit der Client Identität identisch ist. Wenn diese verwendet wird, kann die Client Anwendung eine beliebige Sitzung angeben. in diesem Fall wird der Server als der Benutzer ausgeführt, der die Sitzung besitzt, nicht als der Start Benutzer. Die Standard Zugriffsberechtigungen in diesem Szenario ermöglichen dem Start Benutzer nicht das Aufrufen von Methoden auf dem Server. Die folgenden Sicherheitsrisiken bleiben jedoch bestehen:

-   Wenn der com-Server Schnittstellen verfügbar macht, die nicht von com gesteuert werden, wie z. b. TCP-Ports, Named Pipes, LPC-Ports, freigegebene Speicher Abschnitte usw., können diese vom Start Benutzer verwendet werden, um den Server zu beeinflussen. COM-Objekte, die so konfiguriert sind, dass Sie als interaktiver Benutzer ausgeführt werden, sollten diese Angriffsfläche so weit wie möglich verringern.
-   COM-Objekte können Ihre eigenen Zugriffsberechtigungen festlegen. Wenn das Objekt Zugriffsberechtigungen festlegt, entweder in der AppID-Registrierung oder durch den Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), kann der Benutzer den Server starten, um ihn als ein anderer Benutzer auszuführen, und dann auf das Objekt zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Identität](application-identity.md)
</dt> <dt>

[Benutzer wird gestartet](launching-user.md)
</dt> <dt>

[Dienst Identität](service-identity.md)
</dt> <dt>

[Angegebener Benutzer](specified-user.md)
</dt> </dl>

 

 