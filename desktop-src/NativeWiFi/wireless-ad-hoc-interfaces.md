---
description: Die drahtlos Schnittstelle für die Ad-hoc-Programmierung besteht aus den folgenden Schnittstellen.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Drahtlose Ad-hoc-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354590"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="e211c-103">Drahtlose Ad-hoc-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e211c-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="e211c-104">Die drahtlos Schnittstelle für die Ad-hoc-Programmierung besteht aus den folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="e211c-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="e211c-105">Schnittstellenname</span><span class="sxs-lookup"><span data-stu-id="e211c-105">Interface Name</span></span>                                                                       | <span data-ttu-id="e211c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e211c-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e211c-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="e211c-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="e211c-108">Stellt eine drahtlos Netzwerkschnittstellenkarte (NIC) dar.</span><span class="sxs-lookup"><span data-stu-id="e211c-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="e211c-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="e211c-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="e211c-110">Definiert die von [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)unterstützten Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e211c-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="e211c-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="e211c-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="e211c-112">Erstellt und verwaltet 802,11 Ad-hoc-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="e211c-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="e211c-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="e211c-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="e211c-114">Definiert die von der [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) -Schnittstelle unterstützten Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e211c-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="e211c-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="e211c-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="e211c-116">Stellt ein verfügbares Ad-hoc-Netzwerk Ziel innerhalb des Verbindungs Bereichs dar.</span><span class="sxs-lookup"><span data-stu-id="e211c-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="e211c-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="e211c-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="e211c-118">Definiert die von der [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) -Schnittstelle unterstützten Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e211c-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="e211c-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="e211c-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="e211c-120">Gibt die Sicherheitseinstellungen für ein drahtloses Ad-hoc-Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="e211c-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="e211c-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="e211c-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="e211c-122">Stellt die Auflistung der derzeit sichtbaren 802,11 Ad-hoc-Netzwerkschnittstellen dar.</span><span class="sxs-lookup"><span data-stu-id="e211c-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="e211c-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="e211c-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="e211c-124">Stellt die Auflistung der derzeit sichtbaren 802,11 Ad-hoc-Netzwerke dar.</span><span class="sxs-lookup"><span data-stu-id="e211c-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="e211c-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="e211c-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="e211c-126">Stellt die Auflistung der Sicherheitseinstellungen dar, die jedem sichtbaren drahtlos-Ad-hoc-Netzwerk zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e211c-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="e211c-127">Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e211c-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="e211c-128">Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="e211c-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



