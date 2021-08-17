---
description: Das NetworkService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: NetworkService-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f8256a15b43d9a9c0403067a61f9a7cbf6b9d2df0d78936c4d9c06f6dfd87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889394"
---
# <a name="networkservice-account"></a>NetworkService-Konto

Das NetworkService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird. Dieses Konto wird vom Sicherheitssubsystem nicht erkannt, daher können Sie seinen Namen nicht in einem Aufruf der [**LookupAccountName-Funktion**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) angeben. Sie verfügt über mindestberechtigungen auf dem lokalen Computer und fungiert als Computer im Netzwerk.

Dieses Konto kann in einem Aufruf der Funktionen [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) und [**ChangeServiceConfig angegeben**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) werden. Beachten Sie, dass dieses Konto nicht über ein Kennwort verfügt, sodass alle Kennwortinformationen, die Sie in diesem Aufruf angeben, ignoriert werden. Während das Sicherheitssubsystem diesen Kontonamen lokalisiert, unterstützt der SCM keine lokalisierten Namen. Daher erhalten Sie einen lokalisierten Namen für dieses Konto von der [**LookupAccountSid-Funktion,**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) aber der Name des Kontos muss NT AUTHORITY NetworkService sein, wenn Sie \\ **CreateService** oder **ChangeServiceConfig** aufrufen, unabhängig vom Lokalen, oder es können unerwartete Ergebnisse auftreten.

Ein Dienst, der im Kontext des NetworkService-Kontos ausgeführt wird, stellt den Remoteservern die Anmeldeinformationen des Computers zur Verfügung. Standardmäßig enthält das Remotetoken SIDs für die Gruppen "Jeder" und "Authentifizierte Benutzer". Die Benutzer-SID wird aus dem **SECURITY \_ NETWORK SERVICE \_ \_ RID-Wert** erstellt.

Das NetworkService-Konto verfügt über einen eigenen Unterschlüssel unter dem **Registrierungsschlüssel HKEY \_ USERS.** Daher ist der **Registrierungsschlüssel HKEY \_ CURRENT \_ USER** dem NetworkService-Konto zugeordnet.

Das NetworkService-Konto verfügt über die folgenden Berechtigungen:

-   **SE \_ ASSIGNPRIMARYTOKEN \_ NAME** (deaktiviert)
-   **SE \_ AUDIT \_ NAME** (deaktiviert)
-   **SE \_ CHANGE \_ NOTIFY \_ NAME** (aktiviert)
-   **SE \_ CREATE \_ GLOBAL \_ NAME** (aktiviert)
-   **SE \_ IMPERSONATE \_ NAME** (aktiviert)
-   **SE \_ INCREASE \_ QUOTA \_ NAME** (deaktiviert)
-   **SE \_ SHUTDOWN \_ NAME** (deaktiviert)
-   **SE \_ UNDOCK \_ NAME** (deaktiviert)
-   Alle Berechtigungen, die Benutzern und authentifizierten Benutzern zugewiesen sind

Weitere Informationen finden Sie unter [Dienstsicherheit und Zugriffsrechte.](service-security-and-access-rights.md)

 

 
