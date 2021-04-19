---
description: Wenn WUA erkennt, dass ein Aufrufer nicht über die Berechtigung für den Zugriff auf eine Schnittstelle, Methode oder Eigenschaft verfügt, wird das HRESULT E \_ AccessDenied zurückgegeben.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Sichern von Schnittstellen, Methoden und Eigenschaften in der WUA-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372845"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="d0f29-103">Sichern von Schnittstellen, Methoden und Eigenschaften in der WUA-API</span><span class="sxs-lookup"><span data-stu-id="d0f29-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="d0f29-104">Einige Schnittstellen, Methoden und Eigenschaften von Windows Update-Agent (WUA) sind nur für Aufrufer zugänglich, die zu den folgenden Windows-Sicherheitsgruppen gehören:</span><span class="sxs-lookup"><span data-stu-id="d0f29-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="d0f29-105">Administrator</span><span class="sxs-lookup"><span data-stu-id="d0f29-105">Administrator</span></span>
-   <span data-ttu-id="d0f29-106">Benutzer</span><span class="sxs-lookup"><span data-stu-id="d0f29-106">User</span></span>
-   <span data-ttu-id="d0f29-107">Poweruser</span><span class="sxs-lookup"><span data-stu-id="d0f29-107">Power User</span></span>

<span data-ttu-id="d0f29-108">Wenn WUA erkennt, dass ein Aufrufer nicht über die Berechtigung für den Zugriff auf eine Schnittstelle, Methode oder Eigenschaft verfügt, wird das **HRESULT** E \_ AccessDenied zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0f29-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="d0f29-109">Die folgenden Schnittstellen sind für die Sicherheitsgruppen "Administrator", "Benutzer" und "Hauptbenutzer" verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d0f29-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="d0f29-110">**Iautomaticupdates**</span><span class="sxs-lookup"><span data-stu-id="d0f29-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="d0f29-111">**Iautomaticupdatessettings**</span><span class="sxs-lookup"><span data-stu-id="d0f29-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="d0f29-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="d0f29-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="d0f29-113">**Isysteminformation**</span><span class="sxs-lookup"><span data-stu-id="d0f29-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="d0f29-114">**Iupdatesearcher**</span><span class="sxs-lookup"><span data-stu-id="d0f29-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="d0f29-115">[**Iupdatesession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) und [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="d0f29-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="d0f29-116">Wenn die folgenden Bedingungen zutreffen, schlägt die Suche fehl:</span><span class="sxs-lookup"><span data-stu-id="d0f29-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="d0f29-117">Ein Benutzer, der kein Administrator ist, legt die [**UserLocale-Eigenschaft der IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) -Schnittstelle auf ein Gebiets Schema fest, das einer Sprache entspricht, die nicht auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d0f29-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="d0f29-118">Bei der Suche wird ein updatesearch-Objekt verwendet, das aus dem updatesession-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d0f29-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="d0f29-119">Die folgenden Download Schnittstellen und-Methoden sind für die Administratoren und die Hauptbenutzer Gruppen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d0f29-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="d0f29-120">**Iupdatedownloader**</span><span class="sxs-lookup"><span data-stu-id="d0f29-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="d0f29-121">**Iupdate:: copyfromcache**</span><span class="sxs-lookup"><span data-stu-id="d0f29-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="d0f29-122">**IAutomaticUpdatesSettings2:: checkberechtigung**</span><span class="sxs-lookup"><span data-stu-id="d0f29-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="d0f29-123">Administratoren, Benutzer und Hauptbenutzer können [**IAutomaticUpdatesSettings2:: checkberechtigung**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)anrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="d0f29-124">Die folgenden Installations Schnittstellen,-Methoden und-Eigenschaften sind für die Administrator Gruppen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d0f29-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="d0f29-125">**Iautomaticupdates::P ause**</span><span class="sxs-lookup"><span data-stu-id="d0f29-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="d0f29-126">**Iautomaticupdates:: Resume**</span><span class="sxs-lookup"><span data-stu-id="d0f29-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="d0f29-127">**Iautomaticupdates:: enableservice**</span><span class="sxs-lookup"><span data-stu-id="d0f29-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="d0f29-128">**Iupdateingestaller**</span><span class="sxs-lookup"><span data-stu-id="d0f29-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="d0f29-129">**IsHidden-Eigenschaft von iupdate**</span><span class="sxs-lookup"><span data-stu-id="d0f29-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="d0f29-130">Administratoren, Benutzer und Hauptbenutzer können die Werte der [**IsHidden-Eigenschaft von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="d0f29-131">Allerdings können die Werte nur von Administratoren und Haupt Benutzern festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0f29-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="d0f29-132">**Iupdate:: akzepteula**</span><span class="sxs-lookup"><span data-stu-id="d0f29-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="d0f29-133">Administratoren und Hauptbenutzer können die [**Methode "akzepteula" von iupdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="d0f29-134">**Iautomaticupdatessettings:: Save**</span><span class="sxs-lookup"><span data-stu-id="d0f29-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="d0f29-135">**NotificationLevel-Eigenschaft von iautomaticupdatessettings**</span><span class="sxs-lookup"><span data-stu-id="d0f29-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="d0f29-136">Administratoren, Benutzer und Hauptbenutzer können die Werte der [**notificationLevel-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="d0f29-137">Die Werte können jedoch nur von Administratoren festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0f29-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="d0f29-138">**Scheduledinstallationday-Eigenschaft von iautomaticupdatessettings**</span><span class="sxs-lookup"><span data-stu-id="d0f29-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="d0f29-139">Administratoren, Benutzer und Hauptbenutzer können die Werte der [**Eigenschaft scheduledinstallationday von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="d0f29-140">Die Werte können jedoch nur von Administratoren festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0f29-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="d0f29-141">**Scheduledinstallationtime-Eigenschaft von iautomaticupdatessettings**</span><span class="sxs-lookup"><span data-stu-id="d0f29-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="d0f29-142">Administratoren, Benutzer und Hauptbenutzer können die Werte der [**scheduledinstallationtime-Eigenschaft von iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="d0f29-143">Die Werte können jedoch nur von Administratoren festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0f29-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="d0f29-144">**Includerecommendedupdates-Eigenschaft von IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="d0f29-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="d0f29-145">Administratoren, Benutzer und Hauptbenutzer können die Werte der [**includerecommendedupdates-Eigenschaft von IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)abrufen.</span><span class="sxs-lookup"><span data-stu-id="d0f29-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="d0f29-146">Die Werte können jedoch nur von Administratoren festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0f29-146">However, only administrators can set the values.</span></span>

     

 

 



