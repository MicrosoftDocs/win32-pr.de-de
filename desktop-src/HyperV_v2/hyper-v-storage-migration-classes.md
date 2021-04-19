---
description: Die Hyper-V-Migrations-API definiert die folgenden Programmier Elemente.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Referenz zur Hyper-V-Migrations-API
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343778"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="bdd22-103">Referenz zur Hyper-V-Migrations-API</span><span class="sxs-lookup"><span data-stu-id="bdd22-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="bdd22-104">Die Hyper-V-Migrations-API definiert die folgenden Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="bdd22-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bdd22-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bdd22-105">In this section</span></span>



| <span data-ttu-id="bdd22-106">Thema</span><span class="sxs-lookup"><span data-stu-id="bdd22-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="bdd22-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdd22-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdd22-108">**MSVM \_ migrationjob**</span><span class="sxs-lookup"><span data-stu-id="bdd22-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="bdd22-109">Diese Klasse stellt einen Migrations Vorgangs Auftrag dar, der für die Migration des virtuellen System Migrations Dienstanbieter oder des virtuellen Systems erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bdd22-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="bdd22-110">**MSVM \_ virtualsystemmigrationfunktionen**</span><span class="sxs-lookup"><span data-stu-id="bdd22-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="bdd22-111">Definiert die Möglichkeiten, mit denen ein Client die vom Migrationsdienst bereitgestellten Methoden und den gültigen Bereich der Einstellungsdaten für die virtuelle System Migration ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="bdd22-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="bdd22-112">**MSVM \_ virtualsystemmigrationnetworksettingdata**</span><span class="sxs-lookup"><span data-stu-id="bdd22-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="bdd22-113">Stellt das Netzwerk dar, auf dem der Dienst für die Migration des virtuellen Systems auf die Migration eingehender virtueller Systeme lauscht.</span><span class="sxs-lookup"><span data-stu-id="bdd22-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="bdd22-114">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="bdd22-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="bdd22-115">Stellt den Dienst für die virtuelle System Migration dar.</span><span class="sxs-lookup"><span data-stu-id="bdd22-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="bdd22-116">Sie wird zum Migrieren eines virtuellen Systems oder zum Migrieren des Speichers eines virtuellen Systems von einer Virtualisierungsplattform zu einem anderen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdd22-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="bdd22-117">**MSVM \_ virtualsystemmigrationservicesettingdata**</span><span class="sxs-lookup"><span data-stu-id="bdd22-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="bdd22-118">Stellt die Einstellungen für den Dienst für die virtuelle System Migration auf einem Host dar.</span><span class="sxs-lookup"><span data-stu-id="bdd22-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="bdd22-119">**MSVM \_ virtualsystemmigrationservicesettingdatacomponent**</span><span class="sxs-lookup"><span data-stu-id="bdd22-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="bdd22-120">Eine Zuordnung, die verwendet wird, um die Netzwerkeinstellungen der virtuellen System Migration des virtuellen System Migrations Dienstanbieter darzustellen.</span><span class="sxs-lookup"><span data-stu-id="bdd22-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="bdd22-121">**MSVM \_ virtualsystemmigrationsettingdata**</span><span class="sxs-lookup"><span data-stu-id="bdd22-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="bdd22-122">Stellt die Migrations Einstellungen zum Migrieren eines virtuellen Systems und des Speichers dar, der an ein virtuelles System angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bdd22-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




