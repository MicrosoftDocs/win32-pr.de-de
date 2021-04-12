---
title: Konfigurieren des Microsoft Locator Name Service-Anbieters
description: Sie können den von Ihnen angegebenen Namen Dienstanbieter ändern, indem Sie die Konfigurationsdatei rpkreg. dat bearbeiten, in der die NSP-Parameter und die RPC-Protokoll Einstellungen enthalten sind. Verwenden Sie einen Text-Editor, um NSP-Einträge zu ändern.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310416"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="4384c-104">Konfigurieren des Microsoft Locator Name Service-Anbieters</span><span class="sxs-lookup"><span data-stu-id="4384c-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="4384c-105">Sie können den von Ihnen angegebenen Namen Dienstanbieter ändern, indem Sie die Konfigurationsdatei rpkreg. dat bearbeiten, in der die NSP-Parameter und die RPC-Protokoll Einstellungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4384c-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="4384c-106">Verwenden Sie einen Text-Editor, um NSP-Einträge zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4384c-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="4384c-107">**So konfigurieren Sie den Microsoft Locator Name Service-Anbieter neu**</span><span class="sxs-lookup"><span data-stu-id="4384c-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="4384c-108">Öffnen Sie die Datei rpkreg. dat mit einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="4384c-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="4384c-109">Rpkreg. dat befindet sich im Stammverzeichnis, es sei denn, Sie haben während des Setups einen anderen Pfad angegeben.</span><span class="sxs-lookup"><span data-stu-id="4384c-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="4384c-110">Legen Sie die folgenden Werte für die Registrierungseinträge fest.</span><span class="sxs-lookup"><span data-stu-id="4384c-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="4384c-111">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4384c-111">Registry entry</span></span>                                         | <span data-ttu-id="4384c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4384c-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4384c-113">Software \\ Microsoft \\ RPC- \\ Nameservice- \\ Protokoll</span><span class="sxs-lookup"><span data-stu-id="4384c-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="4384c-114">Die Protokoll Sequenz für das Protokoll, das Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="4384c-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="4384c-115">Der Standardwert ist **ncacn \_ NP**.</span><span class="sxs-lookup"><span data-stu-id="4384c-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="4384c-116">Software \\ Microsoft \\ RPC- \\ Nameservice \\ Network Address</span><span class="sxs-lookup"><span data-stu-id="4384c-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="4384c-117">Der Name des Computers, auf dem der Locator ausgeführt wird und der während der Suche nach Namen Diensten von Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4384c-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="4384c-118">Der Standardwert ist der primäre Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="4384c-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="4384c-119">Software \\ Microsoft \\ RPC- \\ Nameservice- \\ Endpunkt</span><span class="sxs-lookup"><span data-stu-id="4384c-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="4384c-120">Der Name des vom Namensdienst verwendeten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4384c-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="4384c-121">Der Standardwert \\ ist \\ pipelocator.</span><span class="sxs-lookup"><span data-stu-id="4384c-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="4384c-122">Speichern und schließen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="4384c-122">Save and close the file.</span></span>

 

 




