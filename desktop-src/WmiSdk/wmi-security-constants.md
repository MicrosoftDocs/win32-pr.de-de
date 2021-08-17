---
description: WMI überprüft die Zugriffsrechte für Anwendungen und Skripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: WMI-Sicherheitskonst constants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739417"
---
# <a name="wmi-security-constants"></a>WMI-Sicherheitskonst constants

WMI überprüft die Zugriffsrechte für Anwendungen und Skripts für Objekte wie WMI-Namespaces, Drucker, Dienste, DCOM-Anwendungen, Dateien, Freigaben und andere sicherungsfähige Objekte. Der Zugriff auf diese sicherungsfähige Objekte wird durch Zugriffssteuerungseinträge (ACCESS Control Entries, ACE) gesteuert. Jeder ACE enthält Listen, die angeben, welche Gruppen oder Benutzer Zugriff haben. Weitere Informationen zu Sicherheits- und Zugriffssteuerungslisten (ACLs, DACLs oder SACLs) finden Sie unter [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).

Viele Anbietermethoden in WMI, die sich auf sicherungsfähige Objekte auswirken, erfordern, dass der Administrator bestimmte Berechtigungen aktiviert. Welche Version der Berechtigungen Sie verwenden, hängt von der Programmiersprache ab, wie unter [**Privilege Constants (Berechtigungskonst constants) gezeigt.**](privilege-constants.md)

Die Sicherheitskonst constants werden in den folgenden Themen definiert:

-   [**Ereignissicherheitskonst constants**](event-security-constants.md)
-   [**Konstanten für Datei- und Verzeichniszugriffsrechte**](file-and-directory-access-rights-constants.md)
-   [**Namespacezugriffsrechte-Konstanten**](namespace-access-rights-constants.md)
-   [**Namespace-ACE-Flagkonst constants**](namespace-ace-flag-constants.md)
-   [**Namespace-ACE-Typkonst constants**](namespace-ace-type-constants.md)
-   [**Berechtigungskonst constants**](privilege-constants.md)

 

 
