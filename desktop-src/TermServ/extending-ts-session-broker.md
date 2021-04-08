---
title: Erweitern des Terminal Dienste-Sitzungs Brokers
description: Sie können TS \ 160; erweitern. Sitzungs Broker mithilfe der COM-Schnittstelle iwtssbplugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729289"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="dccba-103">Erweitern des Terminal Dienste-Sitzungs Brokers</span><span class="sxs-lookup"><span data-stu-id="dccba-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="dccba-104">Terminal Dienste-Sitzungs Broker (TS-Sitzungs Broker) bestimmt, ob ein Benutzer, der eine Verbindung initiiert, bereits eine Sitzung geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="dccba-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="dccba-105">Wenn dies der Fall ist, leitet der TS-Sitzungs Broker die eingehende Verbindung mit der vorhandenen Sitzung an den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server weiter.</span><span class="sxs-lookup"><span data-stu-id="dccba-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="dccba-106">Wenn dies nicht der Fall ist, leitet der TS-Sitzungs Broker die eingehende Verbindung mit den wenigsten Sitzungen an den RD-Sitzungshost-Server weiter.</span><span class="sxs-lookup"><span data-stu-id="dccba-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="dccba-107">Sie können den TS-Sitzungs Broker mithilfe der COM-Schnittstelle [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) erweitern.</span><span class="sxs-lookup"><span data-stu-id="dccba-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="dccba-108">Sie können diese Schnittstelle verwenden, um Verbindungen mit RD-Sitzungshost Servern sowie eine beliebige Art von Remotedesktopprotokoll (RDP) zu verwalten, z. b. Verbindungen mit virtuellen Gast Computern, auf denen Windows Vista Enterprise zentralisierte Desktop (VECD) auf einem Host für virtuelle Computer mit Windows Server 2008 Hyper-V ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dccba-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="dccba-109">Die [**iwtssbplugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) -Schnittstelle bietet mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="dccba-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="dccba-110">Es ist nicht erforderlich, einen Agent auf dem Client oder auf dem RD-Sitzungshost Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="dccba-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="dccba-111">Das Plug-in kann nahtlos mit anderen Remotedesktopdienste Rollen Diensten interagieren, z. b. Remotedesktop Gateway (RD-Gateway), und von den terminaldienstesitzungsbroker Informationen zu Sitzungs-und Computer Zuständen abhängen.</span><span class="sxs-lookup"><span data-stu-id="dccba-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="dccba-112">Sie können das-Plug-in verwenden, um Verbindungen mit Client-oder Server Geräten zu verwalten, die RDP 5,2 oder höher unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dccba-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="dccba-113">Sie können das Plug-in verwenden, um Windows Vista Enterprise zentralisierten Desktop-Lösungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dccba-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="dccba-114">Beachten Sie beim Implementieren der Methoden dieser Schnittstelle die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="dccba-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="dccba-115">Der TS-Sitzungs Broker kann die Methoden dieses COM-Objekts aus mehreren Threads abrufen.</span><span class="sxs-lookup"><span data-stu-id="dccba-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="dccba-116">Wenn eine der aufgerufenen Methoden nicht sofort und erfolgreich zurückgegeben wird, sendet der TS-Sitzungs Broker keine weiteren Aufrufe an das Plug-in und stellt die systemeigene Lasten Ausgleichs Logik wieder her.</span><span class="sxs-lookup"><span data-stu-id="dccba-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="dccba-117">Um Aufrufe des Plug-ins fortzusetzen, müssen Sie den Terminal Dienste-Sitzungs Broker Dienst neu starten.</span><span class="sxs-lookup"><span data-stu-id="dccba-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="dccba-118">Sie müssen das Plug-in als systemweites com-Objekt registrieren, indem Sie Regsvr32.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="dccba-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="dccba-119">Da der Terminal Dienste-Sitzungs Broker Dienst unter dem Konto "NetworkService" ausgeführt wird, müssen Sie dem Konto "Network Service" die erforderlichen Berechtigungen zum Starten, aktivieren und zugreifen über Dcomcnfg.exe einräumen.</span><span class="sxs-lookup"><span data-stu-id="dccba-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="dccba-120">Der Terminal Dienste-Sitzungs Broker Dienst sucht nach der CLSID des COM-Objekts, das das Plug-in im folgenden Registrierungs Unterschlüssel darstellt:</span><span class="sxs-lookup"><span data-stu-id="dccba-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="dccba-121">**HKEY \_ LOCAL \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **extensibilitypluginclsid**</span><span class="sxs-lookup"><span data-stu-id="dccba-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="dccba-122">Weitere Informationen zu Dcomcnfg.exe finden Sie unter [Aktivieren der com-Sicherheit mithilfe von DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="dccba-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dccba-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dccba-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dccba-124">**Iwtssbplugin**</span><span class="sxs-lookup"><span data-stu-id="dccba-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 