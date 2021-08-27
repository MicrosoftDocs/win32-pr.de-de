---
title: RAS-Verwaltungs-DLL-Funktionen
description: Eine RAS-Verwaltungs-DLL muss alle folgenden Funktionen implementieren und exportieren.
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4ed327cf3114ec4bf7844518f3c1500845450021f80bbd59ddd642de9eeac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036390"
---
# <a name="ras-administration-dll-functions"></a>RAS-Verwaltungs-DLL-Funktionen

Eine RAS-Verwaltungs-DLL muss alle folgenden Funktionen implementieren und exportieren:

-   [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   [**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) oder [ **MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)
-   [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) oder [ **MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)
-   [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

**Windows 2000/NT:** Die RAS-Verwaltungs-DLL muss auch das folgende Funktionspaar implementieren und exportieren: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)

Darüber hinaus muss die RAS-Verwaltungs-DLL eines der folgenden Funktionspaare implementieren und exportieren:

-   [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und [ **MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)
-   [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) und [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)
-   [**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) und [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)
-   [**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) und [ **MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)

Wenn eine der erforderlichen Funktionen nicht implementiert ist, kann der Remotezugriffsdienst nicht gestartet werden.

Eine Verwaltungs-DLL ist nicht erforderlich, um die folgenden Funktionspaare zu implementieren:

-   [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [ **MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)
-   [*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) und [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)

Wenn die DLL jedoch eine Funktion in einem oben aufgeführten Paar implementiert, muss sie auch die andere Funktion im Paar implementieren.

Weitere Informationen zu RAS-Verwaltungs-DLLs finden Sie im Übersichtsthema [RAS-Verwaltungs-DLL](ras-administration-dll.md).

 

 