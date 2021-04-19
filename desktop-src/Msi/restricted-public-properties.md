---
description: In bestimmten Fällen kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste von eingeschränkten Windows Installer öffentlichen Eigenschaften außer Kraft setzen.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Eingeschränkte öffentliche Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350012"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="eba81-103">Eingeschränkte öffentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eba81-103">Restricted Public Properties</span></span>

<span data-ttu-id="eba81-104">Im Fall einer verwalteten Installation muss der Paket Ersteller möglicherweise einschränken, welche [öffentlichen Eigenschaften](public-properties.md) an die Serverseite übermittelt werden, und er kann von einem Benutzer geändert werden, der kein Systemadministrator ist.</span><span class="sxs-lookup"><span data-stu-id="eba81-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="eba81-105">Einige Einschränkungen sind im allgemeinen erforderlich, um eine sichere Umgebung zu verwalten, wenn die Installation erfordert, dass das Installationsprogramm erweiterte Berechtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="eba81-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="eba81-106">Wenn alle der folgenden Bedingungen erfüllt sind, kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste von eingeschränkten öffentlichen Eigenschaften außer Kraft setzen:</span><span class="sxs-lookup"><span data-stu-id="eba81-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="eba81-107">Das System ist Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eba81-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="eba81-108">Der Benutzer ist kein Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="eba81-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="eba81-109">Die Anwendung oder das Produkt wird mit erhöhten Rechten installiert.</span><span class="sxs-lookup"><span data-stu-id="eba81-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="eba81-110">Wenn alle oben genannten Bedingungen erfüllt sind, verwendet das Installationsprogramm standardmäßig die folgende Liste der eingeschränkten öffentlichen Eigenschaften, die von jedem Benutzer geändert werden können:</span><span class="sxs-lookup"><span data-stu-id="eba81-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="eba81-111">**Hinspiel**</span><span class="sxs-lookup"><span data-stu-id="eba81-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="eba81-112">**Afterreboot**</span><span class="sxs-lookup"><span data-stu-id="eba81-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="eba81-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="eba81-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="eba81-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="eba81-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="eba81-115">**Executemode**</span><span class="sxs-lookup"><span data-stu-id="eba81-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="eba81-116">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="eba81-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="eba81-117">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="eba81-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="eba81-118">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="eba81-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="eba81-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="eba81-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="eba81-120">**Limitui**</span><span class="sxs-lookup"><span data-stu-id="eba81-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="eba81-121">**Logaction**</span><span class="sxs-lookup"><span data-stu-id="eba81-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="eba81-122">**Nocompanyname**</span><span class="sxs-lookup"><span data-stu-id="eba81-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="eba81-123">**Nomen Name**</span><span class="sxs-lookup"><span data-stu-id="eba81-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="eba81-124">**Msienforceupgradecomponentrules**</span><span class="sxs-lookup"><span data-stu-id="eba81-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="eba81-125">**Msiinstanceguid**</span><span class="sxs-lookup"><span data-stu-id="eba81-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="eba81-126">**Msinewinstance**</span><span class="sxs-lookup"><span data-stu-id="eba81-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="eba81-127">**Msipatchremove**</span><span class="sxs-lookup"><span data-stu-id="eba81-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="eba81-128">**Patch**</span><span class="sxs-lookup"><span data-stu-id="eba81-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="eba81-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="eba81-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="eba81-130">**Promptrollbackcost**</span><span class="sxs-lookup"><span data-stu-id="eba81-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="eba81-131">**Star**</span><span class="sxs-lookup"><span data-stu-id="eba81-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="eba81-132">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="eba81-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="eba81-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="eba81-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="eba81-134">**Zusetzen**</span><span class="sxs-lookup"><span data-stu-id="eba81-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="eba81-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="eba81-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="eba81-136">**Shortfile-Namen**</span><span class="sxs-lookup"><span data-stu-id="eba81-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="eba81-137">**Kranz**</span><span class="sxs-lookup"><span data-stu-id="eba81-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="eba81-138">**Transformsatsource**</span><span class="sxs-lookup"><span data-stu-id="eba81-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="eba81-139">Der Autor eines Installationspakets kann diese Standardliste erweitern, um zusätzliche öffentliche Eigenschaften mithilfe der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="eba81-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="eba81-140">Wenn Sie die [**enableusercontrol**](-enableusercontrol.md) -Eigenschaft oder die [System Richtlinie](system-policy.md) [enableusercontrol](enableusercontrol.md)festlegen, wird die Liste auf alle öffentlichen Eigenschaften erweitert.</span><span class="sxs-lookup"><span data-stu-id="eba81-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="eba81-141">Alle Benutzer können dann eine beliebige öffentliche Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="eba81-141">All users can then change any public property.</span></span>

<span data-ttu-id="eba81-142">Der Installer legt die [**restrictedusercontrol**](restrictedusercontrol.md) -Eigenschaft fest, wenn die Liste der öffentlichen Eigenschaften, die von Benutzern ohne Administratorrechte an den Server übergeben werden, eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="eba81-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eba81-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eba81-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eba81-144">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eba81-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



