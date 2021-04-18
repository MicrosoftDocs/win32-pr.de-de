---
title: Neuerungen bei der Netzwerkverwaltung
description: Neuerungen bei der Netzwerkverwaltung
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391201"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="c2a1e-103">Neuerungen bei der Netzwerkverwaltung</span><span class="sxs-lookup"><span data-stu-id="c2a1e-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="c2a1e-104">Windows 8 und Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2a1e-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="c2a1e-105">Mit Microsoft Windows 8 werden neue Programmierfunktionen für die Netzwerkverwaltung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="c2a1e-106">Diese neuen Elemente erweitern die Funktionalität der Netzwerkverwaltung zum Erstellen von Bereitstellungs Paketen für Offline-Domänen Beitritts Vorgänge bei der Bereitstellung von Computern mit Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="c2a1e-107">Im folgenden sind die neuen Netzwerk Verwaltungsfunktionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2a1e-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c2a1e-108">**Netkreateprovisioningpackage**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="c2a1e-109">**"Nettrequestprovisioningpackagein Stall"**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="c2a1e-110">Im folgenden sind neue Netzwerk Verwaltungsstrukturen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2a1e-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="c2a1e-111">**netsetup- \_ Bereitstellungs Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="c2a1e-112">**Benutzer \_ Informationen \_ 24**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="c2a1e-113">Die Funktion " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) " wurde auf Windows 8 erweitert, um eine neue Informationsebene zu unterstützen und eine [**Benutzer \_ Info \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) -Struktur mit Benutzerkontoinformationen für ein Konto zurückzugeben, das mit einer Internet Identität verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="c2a1e-114">Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2a1e-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="c2a1e-115">Mit Microsoft Windows 7 werden neue Programmierfunktionen für die Netzwerkverwaltung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="c2a1e-116">Diese Elemente erweitern die Funktionalität der Netzwerkverwaltung, um Offline-Domänen Beitritts Vorgänge bei der Bereitstellung von Computern mit Windows 7 zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="c2a1e-117">Im folgenden sind die neuen Netzwerk Verwaltungsfunktionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2a1e-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c2a1e-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="c2a1e-119">**"Nettrequestofflinedomainjoin"**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="c2a1e-120">Die folgenden vorhandenen Netzwerk Verwaltungsfunktionen wurden verbessert, um zusätzliche Optionen zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="c2a1e-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="c2a1e-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="c2a1e-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2a1e-122">Windows Server 2003</span></span>

<span data-ttu-id="c2a1e-123">Mit Microsoft Windows Server 2003 werden neue Programmierfunktionen für die Netzwerkverwaltung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="c2a1e-124">Diese Elemente erweitern die Funktionalität von Netzwerk Verwaltungs Vorgängen auf Windows Server 2003 und höher.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="c2a1e-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2a1e-125">Windows XP</span></span>

<span data-ttu-id="c2a1e-126">Mit Microsoft Windows XP werden neue Programmierfunktionen für die Netzwerkverwaltung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="c2a1e-127">Diese Elemente erweitern die Funktionalität von Netzwerk Verwaltungs Vorgängen unter Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="c2a1e-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="c2a1e-128">Im folgenden sind die neuen Netzwerk Verwaltungsfunktionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2a1e-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c2a1e-129">**Netaddalternativen Computername**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="c2a1e-130">**"Nettenreeratecomputernames"**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="c2a1e-131">**"Nettremuvealternativen Computername"**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="c2a1e-132">**Netsetprimarycomputername**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="c2a1e-133">**Setnetscheduleaccountinformation**</span><span class="sxs-lookup"><span data-stu-id="c2a1e-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




