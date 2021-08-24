---
title: Herstellen einer DFÜ-Verbindung mit dem Internet
description: Die folgenden Funktionen werden verwendet, um Modemverbindungen zu verarbeiten.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955590"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Herstellen einer DFÜ-Verbindung mit dem Internet

Die folgenden Funktionen werden verwendet, um Modemverbindungen zu verarbeiten.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> WinINet-DFÜ-Funktionen unterstützen keine DFÜ-Verbindungen, SmartCard-Authentifizierung oder Verbindungen, die eine registrierungsbasierte Zertifizierung erfordern.

 

> [!Note]  
> Ab Windows Vista und Windows Server 2008 verwenden die WinINet-DFÜ-Funktionen [die RAS-Funktionen,](/windows/desktop/RRAS/remote-access-service-functions) um eine DFÜ-Verbindung herzustellen. WinINet unterstützt die In der [**RasDialDlg-Funktion dokumentierte**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) Funktionalität.

 

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 