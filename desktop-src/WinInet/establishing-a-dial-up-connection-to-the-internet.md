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
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="177cf-103">Einrichten einer DFÜ-Verbindung mit dem Internet</span><span class="sxs-lookup"><span data-stu-id="177cf-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="177cf-104">Die folgenden Funktionen werden verwendet, um Modemverbindungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="177cf-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="177cf-105">**Internetautodial**</span><span class="sxs-lookup"><span data-stu-id="177cf-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="177cf-106">**Internetautodialhangup**</span><span class="sxs-lookup"><span data-stu-id="177cf-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="177cf-107">**Internetwahl**</span><span class="sxs-lookup"><span data-stu-id="177cf-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="177cf-108">**Internetgetconnectedstate**</span><span class="sxs-lookup"><span data-stu-id="177cf-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="177cf-109">**Internetgetconnectedstateex**</span><span class="sxs-lookup"><span data-stu-id="177cf-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="177cf-110">**Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="177cf-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="177cf-111">**Internetgoonline**</span><span class="sxs-lookup"><span data-stu-id="177cf-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="177cf-112">WinInet-DFÜ-Funktionen unterstützen keine Doppel Wählverbindungen, keine Smartcard-Authentifizierung oder Verbindungen, für die eine Registrierungs basierte Zertifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="177cf-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="177cf-113">Ab Windows Vista und Windows Server 2008 verwenden die WinInet-DFÜ-Funktionen die [RAS-Funktionen](/windows/desktop/RRAS/remote-access-service-functions) , um eine DFÜ-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="177cf-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="177cf-114">WinInet unterstützt die Funktionalität, die in der Funktion " [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) " dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="177cf-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="177cf-115">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="177cf-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="177cf-116">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="177cf-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="177cf-117">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="177cf-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 