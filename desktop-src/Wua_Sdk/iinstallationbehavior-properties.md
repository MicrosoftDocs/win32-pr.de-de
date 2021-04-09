---
description: Die iinstallationbehavior-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Iinstallationbehavior-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958985"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="ef035-103">Iinstallationbehavior-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef035-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="ef035-104">Die [**iinstallationbehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef035-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="ef035-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ef035-105">Property</span></span>                                                                                 | <span data-ttu-id="ef035-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef035-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef035-107">**Canrequestuserinput**</span><span class="sxs-lookup"><span data-stu-id="ef035-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="ef035-108">Ruft einen booleschen Wert ab, der angibt, ob bei der Installation oder Deinstallation eines Updates Benutzereingaben angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="ef035-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="ef035-109">**Auswirkung**</span><span class="sxs-lookup"><span data-stu-id="ef035-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="ef035-110">Ruft eine [**installationimpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) -Enumeration ab, die angibt, wie sich die Installation oder die Installation des Updates auf den Computer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="ef035-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="ef035-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="ef035-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="ef035-112">Ruft eine [**installationrebootbehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) -Enumeration ab, die das Neustart Verhalten angibt, das beim Installieren oder Deinstallieren des Updates auftritt.</span><span class="sxs-lookup"><span data-stu-id="ef035-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="ef035-113">**Requirements-netzwerkkonnektivitätskonnektivität**</span><span class="sxs-lookup"><span data-stu-id="ef035-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="ef035-114">Ruft einen booleschen Wert ab, der angibt, ob die Installation oder die Installation eines Updates Netzwerk Konnektivität erfordert.</span><span class="sxs-lookup"><span data-stu-id="ef035-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



