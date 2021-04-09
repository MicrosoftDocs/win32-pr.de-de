---
description: Wenn terminaldienstedienste aktiviert sind, muss die Gina Winlogon-Unterstützungsfunktionen anrufen, um das Setup für die einzelnen Benutzer abzuschließen, die Anmelde Informationen einer Terminaldienste-Client Sitzung abzufragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung zu trennen. Beachten Sie, dass Gina-DLLs in Windows Vista ignoriert werden.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Terminal Dienste-Gina-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862399"
---
# <a name="terminal-services-gina-functions"></a>Terminal Dienste-Gina-Funktionen

Wenn terminaldienstedienste aktiviert sind, muss die [*Gina*](../secgloss/g-gly.md) [*Winlogon*](../secgloss/w-gly.md) -Unterstützungsfunktionen anrufen, um das Setup für die einzelnen Benutzer abzuschließen, die [*Anmelde*](../secgloss/c-gly.md) Informationen einer Terminaldienste-Client Sitzung abzufragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung zu trennen.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Diese Unterstützungsfunktionen umfassen Folgendes:



| Funktion                                                                     | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Schließt die Einrichtung des Benutzers ab.                                                                    |
| [**Wlxqueryclientanmelde Informationen**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Wird aufgerufen, um die Anmelde Informationen von Remote Clients abzufragen, die keine Internetconnector-Lizenz verwenden. |
| [**Wlxqueryinetconnector-Anmelde Informationen**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Wird aufgerufen, um die Anmelde Informationen von Remote Clients abzufragen, die eine Internetconnector-Lizenz verwenden.     |
| [**Wlxqueryterminalservicesdata**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Wird aufgerufen, um die Konfigurationsinformationen für Terminaldienstebenutzer abzurufen.                                |
| [**Wlxdisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Wird aufgerufen, um die Verbindung mit einer Terminal Dienste-Netzwerksitzung zu trennen                                      |



 

Um auf diese Winlogon-Unterstützungsfunktionen zugreifen zu können, muss die Gina-DLL die [**wlx Dispatch-Struktur der \_ \_ Version \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) verwenden. In der [**wlxaushandlungs**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) -Funktion von Gina müssen beide Parameter mindestens wlx, \_ Version \_ 1 \_ 3, aufweisen.

 

 
