---
title: Einrichten einer DFÜ-Verbindung mit dem Internet
description: Die folgenden Funktionen werden verwendet, um Modemverbindungen zu verarbeiten.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039472"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Einrichten einer DFÜ-Verbindung mit dem Internet

Die folgenden Funktionen werden verwendet, um Modemverbindungen zu verarbeiten.

-   [**Internetautodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**Internetautodialhangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**Internetwahl**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**Internetgetconnectedstate**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**Internetgetconnectedstateex**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**Internet Explorer**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**Internetgoonline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> WinInet-DFÜ-Funktionen unterstützen keine Doppel Wählverbindungen, keine Smartcard-Authentifizierung oder Verbindungen, für die eine Registrierungs basierte Zertifizierung erforderlich ist.

 

> [!Note]  
> Ab Windows Vista und Windows Server 2008 verwenden die WinInet-DFÜ-Funktionen die [RAS-Funktionen](/windows/desktop/RRAS/remote-access-service-functions) , um eine DFÜ-Verbindung herzustellen. WinInet unterstützt die Funktionalität, die in der Funktion " [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) " dokumentiert ist.

 

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 