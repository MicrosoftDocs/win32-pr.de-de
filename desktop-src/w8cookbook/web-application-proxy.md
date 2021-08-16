---
title: Webanwendungsproxy
description: Webanwendungsproxy
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211325"
---
# <a name="web-application-proxy"></a>Webanwendungsproxy

## <a name="platform"></a>Plattform

**Server –** Windows Server 2012 R2  






## <a name="description"></a>Beschreibung

In Windows Server 2012 R2 haben wir einen neuen Dienst namens Web Anwendungsproxy unter der Remotezugriffsrolle hinzugefügt, mit dem Administratoren Anwendungen für den externen Zugriff veröffentlichen können. Dieser Dienst fungiert als Reverseproxy und als Active Directory-Verbunddienste (AD FS)-Proxy (AD FS). Tatsächlich ersetzt dieser Dienst den AD FS Proxydienst, wie er in Windows Server 2012 bekannt war.

Mit dem Web-Anwendungsproxy kann eine Organisation lokale Webressourcen für den externen Zugriff verfügbar machen und gleichzeitig das Risiko dieses Zugriffs verwalten, indem Authentifizierungs- und Autorisierungsrichtlinien auf dem AD FS gesteuert werden.

## <a name="manifestation"></a>Manifestation

Der AD FS-Proxydienst befindet sich nicht mehr unter der rolle "Active Directory-Verbunddienste (AD FS)" (AD FS), wurde jedoch durch den Web-Anwendungsproxy unter der Remotezugriffsrolle ersetzt. Dies stellt eine Erweiterung des AD FS-Proxydiensts dar, indem Reverseproxyfunktionen für die Anwendungsveröffentlichung eingeschlossen werden.

## <a name="solution"></a>Lösung

Um auf die Web-Anwendungsproxy zuzugreifen, können Administratoren zu Server-Manager wechseln und einen neuen Rollen-/Rollendienst hinzufügen. Der Administrator findet die Web-Anwendungsproxy unter der Remotezugriffsrolle.

## <a name="resources"></a>Ressourcen

-   [Lösungsanleitung](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 