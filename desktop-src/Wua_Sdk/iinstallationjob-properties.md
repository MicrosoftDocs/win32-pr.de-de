---
description: Die iinstallationjob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Iinstallationjob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752096"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="ec33f-103">Iinstallationjob-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec33f-103">IInstallationJob Properties</span></span>

<span data-ttu-id="ec33f-104">Die [**iinstallationjob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec33f-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="ec33f-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec33f-105">Property</span></span>                                            | <span data-ttu-id="ec33f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec33f-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec33f-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="ec33f-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="ec33f-108">Ruft das aufruferspezifische Zustands Objekt ab, das an die [**iupdateinstaller. begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) -Methode oder die [**iupdateinstaller. beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec33f-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="ec33f-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="ec33f-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="ec33f-110">Ruft einen Wert ab, der angibt, ob ein Aufrufen der [**iupdateinstaller. begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) -Methode oder der [**iupdateinstaller. beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) -Methode vollständig verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ec33f-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="ec33f-111">**Updates**</span><span class="sxs-lookup"><span data-stu-id="ec33f-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="ec33f-112">Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der bei der Installation oder der Installation angegebenen Updates enthält.</span><span class="sxs-lookup"><span data-stu-id="ec33f-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



