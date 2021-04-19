---
description: Das Network Service-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Network Service-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373242"
---
# <a name="networkservice-account"></a>Network Service-Konto

Das Network Service-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird. Dieses Konto wird vom Sicherheits Subsystem nicht erkannt, sodass Sie seinen Namen nicht in einem aufzurufenden [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) -Funktion angeben können. Er verfügt über minimale Berechtigungen auf dem lokalen Computer und fungiert als Computer im Netzwerk.

Dieses Konto kann in einem aufzurufenden Rückruf [**der Funktionen**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "-Funktion" und " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) " angegeben werden. Beachten Sie, dass dieses Konto nicht über ein Kennwort verfügt, sodass alle Kenn Wort Informationen, die Sie in diesem Bericht angeben, ignoriert werden. Obwohl das Sicherheits Subsystem diesen Kontonamen lokalisiert, unterstützt der SCM keine lokalisierten Namen. Aus diesem Grund erhalten Sie einen lokalisierten Namen für dieses Konto von der [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion. der Name des Kontos muss jedoch NT Authority \\ Network Service lauten, wenn Sie " **kreateservice** " oder " **ChangeServiceConfig**" aufrufen, unabhängig vom Gebiets Schema, oder unerwartete Ergebnisse auftreten können.

Ein Dienst, der im Kontext des Network Service-Kontos ausgeführt wird, stellt die Anmelde Informationen des Computers für Remote Server dar. Standardmäßig enthält das Remote Token SIDs für die Gruppen "jeder" und "authentifizierte Benutzer". Die Benutzer-SID wird aus dem RID-Wert des **Security \_ Network \_ Service \_** erstellt.

Das Network Service-Konto verfügt über einen eigenen Unterschlüssel unter dem Registrierungsschlüssel für **HKEY- \_ Benutzer** . Daher ist der Registrierungsschlüssel des **aktuellen HKEY- \_ \_ Benutzers** dem NetworkService-Konto zugeordnet.

Das Network Service-Konto verfügt über die folgenden Berechtigungen:

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

 

 
