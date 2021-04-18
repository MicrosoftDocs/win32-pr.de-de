---
description: Die msikonfigurireservices-Aktion konfiguriert einen Dienst für das System. Mit dieser Aktion werden die Tabellen "msiserviceconfig" und "msiserviceconfigfailureactions" abgefragt.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Msikonfigurireservices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354872"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="080da-104">Msikonfigurireservices-Aktion</span><span class="sxs-lookup"><span data-stu-id="080da-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="080da-105">Die msikonfigurireservices-Aktion konfiguriert einen Dienst für das System.</span><span class="sxs-lookup"><span data-stu-id="080da-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="080da-106">Mit dieser Aktion werden die Tabellen " [msiserviceconfig](msiserviceconfig-table.md) " und " [msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md) " abgefragt.</span><span class="sxs-lookup"><span data-stu-id="080da-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="080da-107">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="080da-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="080da-108">Diese Aktion ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="080da-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="080da-109">Windows-Dienste bieten die Möglichkeit, vordefinierte Aktionen als Reaktion auf einen Fehler in einem Dienst automatisch auszuführen.</span><span class="sxs-lookup"><span data-stu-id="080da-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="080da-110">Um die programmgesteuerte Einrichtung dieser **Wiederherstellungs Aktionen** zu unterstützen, wenn ein Dienst fehlschlägt, wurde [msiserviceconfigfailureactions](msiserviceconfigfailureactions-table.md) der MSI in Version MSI 5,0 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="080da-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="080da-111">Diese Funktionalität funktioniert jedoch nicht wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="080da-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="080da-112">Um dieses Problem zu umgehen, sollte ein Anwendungsentwickler die **benutzerdefinierte Aktions** Funktionalität in msi verwenden, um **sc.exe** auszuführen und die **Wiederherstellungsoptionen** entsprechend festzulegen.</span><span class="sxs-lookup"><span data-stu-id="080da-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="080da-113">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="080da-113">Sequence Restrictions</span></span>

<span data-ttu-id="080da-114">Diese Standardaktion muss in der folgenden Reihenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="080da-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="080da-115">Stop Services</span><span class="sxs-lookup"><span data-stu-id="080da-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="080da-116">Delta Service Services</span><span class="sxs-lookup"><span data-stu-id="080da-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="080da-117">Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".</span><span class="sxs-lookup"><span data-stu-id="080da-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="080da-118">Installdienste</span><span class="sxs-lookup"><span data-stu-id="080da-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="080da-119">Msikonfigurireservices</span><span class="sxs-lookup"><span data-stu-id="080da-119">MsiConfigureServices</span></span>

[<span data-ttu-id="080da-120">Startdienste</span><span class="sxs-lookup"><span data-stu-id="080da-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="080da-121">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="080da-121">ActionData Messages</span></span>

<span data-ttu-id="080da-122">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="080da-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="080da-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="080da-123">Remarks</span></span>

<span data-ttu-id="080da-124">Für diese Aktion ist es erforderlich, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Installieren von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.</span><span class="sxs-lookup"><span data-stu-id="080da-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



