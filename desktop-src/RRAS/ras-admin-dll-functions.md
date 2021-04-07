---
title: Funktionen der RAS-Verwaltungs-dll
description: 'Eine RAS-Verwaltungs-dll muss alle folgenden Funktionen implementieren und exportieren:'
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a02c8dc9212f3cfd173c9a236f81fcf766658424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729097"
---
# <a name="ras-administration-dll-functions"></a>Funktionen der RAS-Verwaltungs-dll

Eine RAS-Verwaltungs-dll muss alle folgenden Funktionen implementieren und exportieren:

-   [**Mpradminakzeptnewlink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   [**Mpradminaccept treauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) oder [ **mpradminakzeptreauthenticationex**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)
-   [**Mpradmininitializedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) oder [ **mpradmininitializedllex**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)
-   [**Mpradminlinkhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [**Mpradminterminatedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

**Windows 2000/NT:** Die RAS-Verwaltungs-dll muss auch das folgende Funktions paar implementieren und exportieren: [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)

Außerdem muss die RAS-Verwaltungs-dll eines der folgenden Funktions Paare implementieren und exportieren:

-   [**Mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und [ **mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)
-   [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) und [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)
-   [**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) und [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)
-   [**Mpradminaccept tnewconnectionex**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) und [ **mpradminconnectionhangupnotificationex**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)

Wenn eine der erforderlichen Funktionen nicht implementiert ist, kann der Remote Zugriffs Dienst nicht gestartet werden.

Eine Verwaltungs-dll ist nicht erforderlich, um die folgenden Funktions Paare zu implementieren:

-   [**Mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [ **mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)
-   [*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) und [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)

Wenn die dll jedoch eine Funktion in einem oben aufgelisteten paar implementiert, muss Sie auch die andere Funktion im Paar implementieren.

Weitere Informationen zu RAS-Verwaltungs-DLLs finden Sie im Übersichts Thema [RAS-Verwaltungs-dll](ras-administration-dll.md).

 

 