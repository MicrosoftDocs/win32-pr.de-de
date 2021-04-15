---
title: Konfigurieren des Namens Dienstanbieter
description: Ab Windows 2000 wählt das Setup Programm beim Installieren des Windows SDK automatisch Microsoft Locator als Name Service Provider aus. Sie können den Namen des Dienstanbieters über die Systemsteuerung ändern.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471229"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="deb23-104">Konfigurieren des Namens Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="deb23-104">Configuring the Name Service</span></span>

<span data-ttu-id="deb23-105">Ab Windows 2000 wählt das Setup Programm beim Installieren des Windows SDK automatisch Microsoft Locator als Name Service Provider aus.</span><span class="sxs-lookup"><span data-stu-id="deb23-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="deb23-106">Sie können den Namen des Dienstanbieters über die Systemsteuerung ändern.</span><span class="sxs-lookup"><span data-stu-id="deb23-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="deb23-107">Der Host Computer, der die nsid ausführt, fungiert als Gateway für den DCE-Zell Verzeichnisdienst und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="deb23-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="deb23-108">Eine Netzwerkadresse kann bis zu 80 Zeichen lang sein – z. b. 11.1.9.169 ist eine gültige Adresse.</span><span class="sxs-lookup"><span data-stu-id="deb23-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="deb23-109">Sie müssen über das DCE CDs-Produkt der Digital Equipment Corporation verfügen, um die DCE-CDs als Name Service Provider zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="deb23-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="deb23-110">Weitere Informationen zu DCE CDs finden Sie in der Dokumentation der Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="deb23-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="deb23-111">**So konfigurieren Sie den Namen Dienstanbieter neu**</span><span class="sxs-lookup"><span data-stu-id="deb23-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="deb23-112">Klicken Sie in der Systemsteuerung auf das Symbol " **Netzwerkverbindungen** ".</span><span class="sxs-lookup"><span data-stu-id="deb23-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="deb23-113">Das Fenster **Netzwerkverbindungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb23-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="deb23-114">Wählen Sie die zu konfigurier Netzwerkverbindung aus, klicken Sie mit der rechten Maustaste, und wählen Sie im Kontextmenü **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="deb23-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="deb23-115">Das Dialogfeld **Verbindungs Eigenschaften** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb23-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="deb23-116">Wählen Sie im Dialogfeld **Verbindungs Eigenschaften** die Option **Client für Microsoft-Netzwerke** , und klicken Sie auf die Schaltfläche **Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="deb23-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="deb23-117">Das Dialogfeld **Client für Microsoft-Netzwerk Eigenschaften** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb23-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="deb23-118">Öffnen Sie im Dialogfeld **Client für Microsoft-Netzwerk Eigenschaften** die Dropdown Liste **Name Service Provider** , und wählen Sie einen Namen Anbieter aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="deb23-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="deb23-119">Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="deb23-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="deb23-120">Der Konfigurations Vorgang ist dann beendet.</span><span class="sxs-lookup"><span data-stu-id="deb23-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="deb23-121">Wenn Sie den DCE-Zell Verzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Host Computers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.</span><span class="sxs-lookup"><span data-stu-id="deb23-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="deb23-122">**So konfigurieren Sie den Namen Dienstanbieter für Windows 2000 neu**</span><span class="sxs-lookup"><span data-stu-id="deb23-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="deb23-123">Klicken Sie in der Systemsteuerung auf das **Netzwerk** Symbol.</span><span class="sxs-lookup"><span data-stu-id="deb23-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="deb23-124">Das Dialogfeld **Netzwerk** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb23-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="deb23-125">Klicken Sie im Dialogfeld **Netzwerk** auf **Konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="deb23-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="deb23-126">Wählen Sie in der Liste **networksoftware** die Option **RPC-Konfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="deb23-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="deb23-127">Das Dialogfeld **Konfiguration des RPC-namens Dienstanbieters** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="deb23-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="deb23-128">Wählen Sie im Dialogfeld **Konfiguration des RPC-namens Dienstanbieters** in der Liste einen Namen Dienstanbieter aus.</span><span class="sxs-lookup"><span data-stu-id="deb23-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="deb23-129">Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="deb23-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="deb23-130">Der Konfigurations Vorgang ist dann beendet.</span><span class="sxs-lookup"><span data-stu-id="deb23-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="deb23-131">Wenn Sie den DCE-Zell Verzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Host Computers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.</span><span class="sxs-lookup"><span data-stu-id="deb23-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 




