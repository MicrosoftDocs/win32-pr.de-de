---
description: Das LocalService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: LocalService-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529867"
---
# <a name="localservice-account"></a>LocalService-Konto

Das LocalService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird. Er verfügt über minimale Berechtigungen auf dem lokalen Computer und stellt anonyme Anmelde Informationen im Netzwerk dar.

Dieses Konto kann in einem aufzurufenden Rückruf [**der Funktionen**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "-Funktion" und " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) " angegeben werden. Beachten Sie, dass dieses Konto nicht über ein Kennwort verfügt, sodass alle Kenn Wort Informationen, die Sie in diesem Bericht angeben, ignoriert werden. Obwohl das Sicherheits Subsystem diesen Kontonamen lokalisiert, unterstützt der SCM keine lokalisierten Namen. Daher erhalten Sie einen lokalisierten Namen für dieses Konto von der [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion, aber der Name des Kontos muss NT Authority \\ LocalService lauten, wenn Sie " **kreateservice** " oder " **ChangeServiceConfig**" aufrufen, unabhängig vom Gebiets Schema oder unerwartete Ergebnisse können auftreten.

Die Benutzer-SID wird aus dem RID-Wert des **\_ lokalen \_ \_ Diensts der Sicherheit** erstellt.

Das LocalService-Konto verfügt über einen eigenen Unterschlüssel unter dem Registrierungsschlüssel " **HKEY \_ Users** ". Daher ist der Registrierungsschlüssel des **aktuellen HKEY- \_ \_ Benutzers** dem LocalService-Konto zugeordnet.

Das LocalService-Konto verfügt über die folgenden Berechtigungen:

-   **SE \_ \_Name des zugriffsmarytokens** (deaktiviert)
-   **SE \_ Überwachungs \_ Name** (deaktiviert)
-   **SE \_ \_Benachrichtigungs \_ Name ändern** (aktiviert)
-   **SE \_ \_Globalen \_ Namen erstellen** (aktiviert)
-   **SE \_ Identität des \_ namens** annehmen (aktiviert)
-   **SE \_ \_Kontingent \_ Namen erhöhen** (deaktiviert)
-   **SE \_ \_Name des herunter** Fahrens (deaktiviert)
-   **SE \_ \_Name der nicht-Dock** (deaktiviert)
-   Alle Berechtigungen, die Benutzern und authentifizierten Benutzern zugewiesen sind

Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](service-security-and-access-rights.md).

 

 
