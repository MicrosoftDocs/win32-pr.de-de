---
description: Wenn Terminaldienste aktiviert sind, muss die GINA Winlogon-Supportfunktionen aufrufen, um das Setup für jeden Benutzer abzuschließen, die Anmeldeinformationen einer Terminaldienste-Clientsitzung abfragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung trennen zu können. Beachten Sie, dass GINA-DLLs in Windows Vista ignoriert werden.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: GINA-Funktionen für Terminaldienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bdd81d66d88ae280c14d71d7d65385c0d5580b3e28cef9d0f26ed1963bded1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916392"
---
# <a name="terminal-services-gina-functions"></a>GINA-Funktionen für Terminaldienste

Wenn Terminaldienste aktiviert sind, muss [*die GINA Winlogon-Supportfunktionen*](../secgloss/g-gly.md) aufrufen, [](../secgloss/c-gly.md) um das Setup für jeden Benutzer abzuschließen, die Anmeldeinformationen einer Terminaldienste-Clientsitzung abfragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung trennen zu können. [](../secgloss/w-gly.md)

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Diese Unterstützungsfunktionen umfassen Folgendes:



| Funktion                                                                     | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Schließt die Einrichtung des Benutzers ab.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Wird aufgerufen, um die Anmeldeinformationen von Remoteclients zu abfragen, die keine Internetconnectorlizenz verwenden. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Wird aufgerufen, um die Anmeldeinformationen von Remoteclients zu abfragen, die eine Internetconnectorlizenz verwenden.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Wird aufgerufen, um Benutzerkonfigurationsinformationen für Terminaldienste abzurufen.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Wird aufgerufen, um die Verbindung mit einer Terminaldienste-Netzwerksitzung zu trennen.                                      |



 

Für den Zugriff auf diese Winlogon-Unterstützungsfunktionen muss die GINA-DLL die [**WLX \_ DISPATCH \_ VERSION \_ 1 \_ 3-Struktur**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) verwenden. In der [**WlxNegotiate-Funktion**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) der GINA müssen beide Parameter mindestens WLX \_ VERSION \_ 1 \_ 3 sein.

 

 
