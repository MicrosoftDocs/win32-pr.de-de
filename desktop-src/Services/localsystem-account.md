---
description: Das LocalSystem-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: LocalSystem-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d4dca5655402b3b4f400d3c1941ccf3978a7d385363567fac01a1d3024f1dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889441"
---
# <a name="localsystem-account"></a>LocalSystem-Konto

Das LocalSystem-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird. Dieses Konto wird vom Sicherheitssubsystem nicht erkannt, daher können Sie seinen Namen nicht in einem Aufruf der [**LookupAccountName-Funktion**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) angeben. Sie verfügt über umfassende Berechtigungen auf dem lokalen Computer und fungiert als Computer im Netzwerk. Das Token enthält die SIDs NT AUTHORITY \\ SYSTEM und BUILTIN Administrators. Diese Konten haben Zugriff auf die meisten \\ Systemobjekte. Der Name des Kontos in allen Lokalen ist . \\ Localsystem. Der Name LocalSystem oder *ComputerName* \\ LocalSystem kann ebenfalls verwendet werden. Dieses Konto verfügt nicht über ein Kennwort. Wenn Sie das LocalSystem-Konto in einem Aufruf der [**Funktion CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) oder [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) angeben, werden alle von Ihnen angegebenen Kennwortinformationen ignoriert.

Ein Dienst, der im Kontext des LocalSystem-Kontos ausgeführt wird, erbt den Sicherheitskontext des SCM. Die Benutzer-SID wird aus dem **SECURITY \_ LOCAL SYSTEM \_ \_ RID-Wert** erstellt. Das Konto ist mit keinen angemeldeten Benutzerkonten verknüpft. Das hat eine Reihe von Auswirkungen:

-   Der Registrierungsschlüssel **HKEY \_ CURRENT \_ USER** ist dem Standardbenutzer zugeordnet, nicht dem aktuellen Benutzer. Um auf das Profil eines anderen Benutzers zu zugreifen, geben Sie die Identität des Benutzers an, und greifen Sie dann **auf HKEY \_ CURRENT USER \_ zu.**
-   Der Dienst kann den Registrierungsschlüssel **HKEY \_ LOCAL MACHINE \_ SECURITY \\ öffnen.**
-   Der Dienst stellt die Anmeldeinformationen des Computers für Remoteserver zur Verfügung.
-   Wenn der Dienst ein Befehlsfenster öffnet und eine Batchdatei ausgeführt, kann der Benutzer STRG+C drücken, um die Batchdatei zu beenden und Zugriff auf ein Befehlsfenster mit LocalSystem-Berechtigungen zu erhalten.

Das LocalSystem-Konto verfügt über die folgenden Berechtigungen:

-   **SE \_ ASSIGNPRIMARYTOKEN \_ NAME** (deaktiviert)
-   **SE \_ AUDIT \_ NAME** (aktiviert)
-   **SE \_ BACKUP \_ NAME** (deaktiviert)
-   **SE \_ CHANGE \_ NOTIFY \_ NAME** (aktiviert)
-   **SE \_ CREATE \_ GLOBAL \_ NAME** (aktiviert)
-   **SE \_ CREATE \_ PAGEFILE \_ NAME** (aktiviert)
-   **SE \_ CREATE \_ PERMANENT \_ NAME** (aktiviert)
-   **SE \_ CREATE \_ TOKEN \_ NAME** (deaktiviert)
-   **SE \_ \_DEBUGNAME** (aktiviert)
-   **SE \_ IMPERSONATE \_ NAME** (aktiviert)
-   **SE \_ INC \_ BASE \_ PRIORITY \_ NAME** (aktiviert)
-   **SE \_ INCREASE \_ QUOTA \_ NAME** (deaktiviert)
-   **SE \_ LOAD \_ DRIVER \_ NAME** (deaktiviert)
-   **SE \_ LOCK \_ MEMORY \_ NAME** (aktiviert)
-   **SE \_ MANAGE \_ VOLUME \_ NAME** (deaktiviert)
-   **SE \_ PROF \_ SINGLE \_ PROCESS \_ NAME** (aktiviert)
-   **SE \_ RESTORE \_ NAME** (deaktiviert)
-   **SE \_ \_SICHERHEITSNAME** (deaktiviert)
-   **SE \_ SHUTDOWN \_ NAME** (deaktiviert)
-   **SE \_ \_ \_ SYSTEMUMGEBUNGSNAME** (deaktiviert)
-   **SE \_ SYSTEMTIME \_ NAME** (deaktiviert)
-   **SE \_ TAKE \_ OWNERSHIP \_ NAME** (deaktiviert)
-   **SE \_ \_TCB-NAME** (aktiviert)
-   **SE \_ UNDOCK \_ NAME** (deaktiviert)

Die meisten Dienste benötigen keine so hohe Berechtigungsstufe. Wenn Ihr Dienst diese Berechtigungen nicht benötigt und es sich nicht um einen interaktiven Dienst handelt, ziehen Sie die Verwendung des [LocalService-Kontos](localservice-account.md) oder des [NetworkService-Kontos in Betracht.](networkservice-account.md) Weitere Informationen finden Sie unter [Dienstsicherheit und Zugriffsrechte.](service-security-and-access-rights.md)

 

 
