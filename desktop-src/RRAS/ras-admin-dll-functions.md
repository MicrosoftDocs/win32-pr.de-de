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
# <a name="ras-administration-dll-functions"></a><span data-ttu-id="b069e-103">Funktionen der RAS-Verwaltungs-dll</span><span class="sxs-lookup"><span data-stu-id="b069e-103">RAS administration DLL functions</span></span>

<span data-ttu-id="b069e-104">Eine RAS-Verwaltungs-dll muss alle folgenden Funktionen implementieren und exportieren:</span><span class="sxs-lookup"><span data-stu-id="b069e-104">A RAS administration DLL must implement and export all of the following functions:</span></span>

-   [<span data-ttu-id="b069e-105">**Mpradminakzeptnewlink**</span><span class="sxs-lookup"><span data-stu-id="b069e-105">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   <span data-ttu-id="b069e-106">[**Mpradminaccept treauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) oder [ **mpradminakzeptreauthenticationex**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span><span class="sxs-lookup"><span data-stu-id="b069e-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) or [**MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span></span>
-   <span data-ttu-id="b069e-107">[**Mpradmininitializedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) oder [ **mpradmininitializedllex**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span><span class="sxs-lookup"><span data-stu-id="b069e-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) or [**MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span></span>
-   [<span data-ttu-id="b069e-108">**Mpradminlinkhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="b069e-108">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [<span data-ttu-id="b069e-109">**Mpradminterminatedll**</span><span class="sxs-lookup"><span data-stu-id="b069e-109">**MprAdminTerminateDll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

<span data-ttu-id="b069e-110">**Windows 2000/NT:** Die RAS-Verwaltungs-dll muss auch das folgende Funktions paar implementieren und exportieren: [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="b069e-110">**Windows 2000/NT:** The RAS administration DLL must also implement and export the following pair of functions: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>

<span data-ttu-id="b069e-111">Außerdem muss die RAS-Verwaltungs-dll eines der folgenden Funktions Paare implementieren und exportieren:</span><span class="sxs-lookup"><span data-stu-id="b069e-111">In addition, the RAS administration DLL must implement and export one of the following pairs of functions:</span></span>

-   <span data-ttu-id="b069e-112">[**Mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und [ **mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span><span class="sxs-lookup"><span data-stu-id="b069e-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) and [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span></span>
-   <span data-ttu-id="b069e-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) und [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span><span class="sxs-lookup"><span data-stu-id="b069e-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) and [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span></span>
-   <span data-ttu-id="b069e-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) und [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span><span class="sxs-lookup"><span data-stu-id="b069e-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) and [**MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span></span>
-   <span data-ttu-id="b069e-115">[**Mpradminaccept tnewconnectionex**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) und [ **mpradminconnectionhangupnotificationex**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span><span class="sxs-lookup"><span data-stu-id="b069e-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) and [**MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span></span>

<span data-ttu-id="b069e-116">Wenn eine der erforderlichen Funktionen nicht implementiert ist, kann der Remote Zugriffs Dienst nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b069e-116">If one of the required functions is not implemented, the remote access service fails to start.</span></span>

<span data-ttu-id="b069e-117">Eine Verwaltungs-dll ist nicht erforderlich, um die folgenden Funktions Paare zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="b069e-117">An administration DLL is not required to implement the following pairs of functions:</span></span>

-   <span data-ttu-id="b069e-118">[**Mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [ **mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="b069e-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>
-   <span data-ttu-id="b069e-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) und [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span><span class="sxs-lookup"><span data-stu-id="b069e-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) and [*MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span></span>

<span data-ttu-id="b069e-120">Wenn die dll jedoch eine Funktion in einem oben aufgelisteten paar implementiert, muss Sie auch die andere Funktion im Paar implementieren.</span><span class="sxs-lookup"><span data-stu-id="b069e-120">However, if the DLL implements one function in a pair listed above, it must implement the other function in the pair as well.</span></span>

<span data-ttu-id="b069e-121">Weitere Informationen zu RAS-Verwaltungs-DLLs finden Sie im Übersichts Thema [RAS-Verwaltungs-dll](ras-administration-dll.md).</span><span class="sxs-lookup"><span data-stu-id="b069e-121">For more information on RAS Administration DLLs, see the overview topic, [RAS Administration DLL](ras-administration-dll.md).</span></span>

 

 