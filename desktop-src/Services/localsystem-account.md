---
description: Das LocalSystem-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: LocalSystem-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958818"
---
# <a name="localsystem-account"></a>LocalSystem-Konto

Das LocalSystem-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird. Dieses Konto wird vom Sicherheits Subsystem nicht erkannt, sodass Sie seinen Namen nicht in einem aufzurufenden [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) -Funktion angeben können. Sie verfügt über umfangreiche Berechtigungen auf dem lokalen Computer und fungiert als Computer im Netzwerk. Das zugehörige Token enthält die \\ SIDs NT Authority System und Builtin \\ Administrators. diese Konten haben Zugriff auf die meisten System Objekte. Der Name des Kontos in allen Gebiets Schemas ist. \\ LocalSystem. Der Name, LocalSystem oder *Computername* \\ LocalSystem kann ebenfalls verwendet werden. Dieses Konto weist kein Kennwort auf. Wenn Sie das Konto "LocalSystem" in einem [**Aufrufen der Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "" von " [](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) " "" "" "" "" "" "" "" "" "" "" "," ""

Ein Dienst, der im Kontext des Kontos "LocalSystem" ausgeführt wird, erbt den Sicherheitskontext des SCM. Die Benutzer-SID wird aus dem RID-Wert des **\_ lokalen Sicherheits \_ Systems \_** erstellt. Das Konto ist keinem angemeldeten Benutzerkonto zugeordnet. Das hat eine Reihe von Auswirkungen:

-   Der **\_ aktuelle \_ Benutzer** des Registrierungsschlüssels HKEY ist dem Standardbenutzer zugeordnet, nicht dem aktuellen Benutzer. Wenn Sie auf das Profil eines anderen Benutzers zugreifen möchten, müssen Sie die Identität des Benutzers annehmen und dann auf **HKEY \_ aktueller \_ Benutzer** zugreifen.
-   Der Dienst kann den Registrierungsschlüssel **HKEY \_ lokale \_ Computer \\ Sicherheit** öffnen.
-   Der Dienst stellt die Anmelde Informationen des Computers für Remote Server dar.
-   Wenn der Dienst ein Befehlsfenster öffnet und eine Batchdatei ausführt, könnte der Benutzer STRG + C drücken, um die Batchdatei zu beenden und mit LocalSystem-Berechtigungen Zugriff auf ein Befehlsfenster zu erhalten.

Das LocalSystem-Konto verfügt über die folgenden Berechtigungen:

-   **SE \_ \_Name des zugriffsmarytokens** (deaktiviert)
-   **SE \_ Überwachungs \_ Name** (aktiviert)
-   **SE \_ Sicherungs \_ Name** (deaktiviert)
-   **SE \_ \_Benachrichtigungs \_ Name ändern** (aktiviert)
-   **SE \_ \_Globalen \_ Namen erstellen** (aktiviert)
-   **SE \_ \_Pagefile- \_ Namen erstellen** (aktiviert)
-   **SE \_ \_Permanenten \_ Namen erstellen** (aktiviert)
-   **SE \_ \_ \_ Tokenname erstellen** (deaktiviert)
-   **SE \_ \_Debugname** (aktiviert)
-   **SE \_ Identität des \_ namens** annehmen (aktiviert)
-   **SE \_ \_ \_ \_ Name der Basis Priorität** (aktiviert)
-   **SE \_ \_Kontingent \_ Namen erhöhen** (deaktiviert)
-   **SE \_ \_Treiber \_ Namen laden** (deaktiviert)
-   **SE \_ \_ \_ Name des Sperr Speichers** (aktiviert)
-   **SE \_ \_ \_ Volumename verwalten** (deaktiviert)
-   **SE \_ Name für einen \_ einzelnen \_ Prozess \_ in Prof** (aktiviert)
-   **SE \_ \_Name der Wiederherstellung** (deaktiviert)
-   **SE \_ Sicherheits \_ Name** (deaktiviert)
-   **SE \_ \_Name des herunter** Fahrens (deaktiviert)
-   **SE \_ \_ \_ Name der System Umgebung** (deaktiviert)
-   **SE \_ \_Systemzeitname** (deaktiviert)
-   **SE \_ \_Besitz \_ Namen übernehmen** (deaktiviert)
-   **SE \_ TCB- \_ Name** (aktiviert)
-   **SE \_ \_Name der nicht-Dock** (deaktiviert)

Die meisten Dienste benötigen nicht eine solche hohe Berechtigungsstufe. Wenn Ihr Dienst diese Berechtigungen nicht benötigt und es sich nicht um einen interaktiven Dienst handelt, sollten Sie das [LocalService-Konto](localservice-account.md) oder das [Network Service-Konto](networkservice-account.md)verwenden. Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](service-security-and-access-rights.md).

 

 
