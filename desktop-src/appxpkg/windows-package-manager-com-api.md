---
title: Windows-Paket-Manager com-API
description: Gilt für Windows 10 und ist in der Familie mobiler Geräte implementiert. Wenn Sie weitere Informationen zum Windows-Paket-Manager haben, wenden Sie sich an Ihren Microsoft-Kundenbetreuer.
ms.assetid: 4863EC42-413D-46E3-AE61-E29006708E39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82de491b2ceb7da7029a8db7fdf3e436a92d50a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338973"
---
# <a name="windows-package-manager-com-api"></a><span data-ttu-id="3b146-104">Windows-Paket-Manager com-API</span><span class="sxs-lookup"><span data-stu-id="3b146-104">Windows Package Manager COM API</span></span>

<span data-ttu-id="3b146-105">Gilt für Windows 10 und ist in der Familie mobiler Geräte implementiert.</span><span class="sxs-lookup"><span data-stu-id="3b146-105">Applies to Windows 10, and implemented in the mobile device family.</span></span> <span data-ttu-id="3b146-106">Wenn Sie weitere Informationen zum Windows-Paket-Manager haben, wenden Sie sich an Ihren Microsoft-Kundenbetreuer.</span><span class="sxs-lookup"><span data-stu-id="3b146-106">For more information about Windows Package Manager, please work with your Microsoft Account Team representative.</span></span>

> [!Note]
>
> <span data-ttu-id="3b146-107">Diese API ist nicht für alle Windows-apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b146-107">This API is not available to all Windows apps.</span></span> <span data-ttu-id="3b146-108">Wenn Ihr Entwicklerkonto nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="3b146-108">Unless your developer account is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

 

<span data-ttu-id="3b146-109">Die API besteht aus der folgenden Co-Klasse.</span><span class="sxs-lookup"><span data-stu-id="3b146-109">The API consists of the following coclass.</span></span>

-   <span data-ttu-id="3b146-110">Pmsvc.</span><span class="sxs-lookup"><span data-stu-id="3b146-110">PMSvc.</span></span> <span data-ttu-id="3b146-111">CLSID: {B9E511FC-E364-497A-a1-21-B7-B3-61-2C-Ed-CE}</span><span class="sxs-lookup"><span data-stu-id="3b146-111">CLSID: {B9E511FC-E364-497A-A1-21-B7-B3-61-2C-ED-CE}</span></span>

<span data-ttu-id="3b146-112">Pmsvc implementiert die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3b146-112">PMSvc implements the following interfaces.</span></span>

-   <span data-ttu-id="3b146-113">Ipmapplicationinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-113">IPMApplicationInfo.</span></span> <span data-ttu-id="3b146-114">IID: {50afb58a-438c-4088-97-89-F8-C4-89-98 -29-C7}</span><span class="sxs-lookup"><span data-stu-id="3b146-114">IID: {50AFB58A-438C-4088-97-89-F8-C4-89-98-29-C7}</span></span>
-   <span data-ttu-id="3b146-115">Ipmtilepropertyinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-115">IPMTilePropertyInfo.</span></span> <span data-ttu-id="3b146-116">IID: {6c2b8017-1efa-42a7-86-C0-6D-4B-64-0B-F5-28}</span><span class="sxs-lookup"><span data-stu-id="3b146-116">IID: {6C2B8017-1EFA-42a7-86-C0-6D-4B-64-0B-F5-28}</span></span>
-   <span data-ttu-id="3b146-117">Ipmtilepropertyenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-117">IPMTilePropertyEnumerator.</span></span> <span data-ttu-id="3b146-118">IID: {CC4CD629-9047 -4250-AA-C8-93-0E-47-81-24-21}</span><span class="sxs-lookup"><span data-stu-id="3b146-118">IID: {CC4CD629-9047-4250-AA-C8-93-0E-47-81-24-21}</span></span>
-   <span data-ttu-id="3b146-119">Ipmtileingefo.</span><span class="sxs-lookup"><span data-stu-id="3b146-119">IPMTileInfo.</span></span> <span data-ttu-id="3b146-120">IID: {D1604833-2b08-4001 -82-CD-18-3a-T7-34-F7-52}</span><span class="sxs-lookup"><span data-stu-id="3b146-120">IID: {D1604833-2B08-4001-82-CD-18-3A-D7-34-F7-52}</span></span>
-   <span data-ttu-id="3b146-121">Ipmtileingefoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-121">IPMTileInfoEnumerator.</span></span> <span data-ttu-id="3b146-122">IID: {DED83065-e462-4b2c-AC-B5-E3-9c-EA-61-C8-74}</span><span class="sxs-lookup"><span data-stu-id="3b146-122">IID: {DED83065-E462-4b2c-AC-B5-E3-9C-EA-61-C8-74}</span></span>
-   <span data-ttu-id="3b146-123">Ipmapplicationinfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-123">IPMApplicationInfoEnumerator.</span></span> <span data-ttu-id="3b146-124">IID: {0ec42a96-4D46-4dc6-a3-D9-A7-AC-AA-C0-F5-FA}</span><span class="sxs-lookup"><span data-stu-id="3b146-124">IID: {0EC42A96-4D46-4dc6-A3-D9-A7-AC-AA-C0-F5-FA}</span></span>
-   <span data-ttu-id="3b146-125">Ipmlivetilejobinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-125">IPMLiveTileJobInfo.</span></span> <span data-ttu-id="3b146-126">IID: {6009a81f-4710-4697-B5-F6-22 -08-F6-05-7B-8E}</span><span class="sxs-lookup"><span data-stu-id="3b146-126">IID: {6009A81F-4710-4697-B5-F6-22-08-F6-05-7B-8E}</span></span>
-   <span data-ttu-id="3b146-127">Ipmlivetilejobinfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-127">IPMLiveTileJobInfoEnumerator.</span></span> <span data-ttu-id="3b146-128">IID: {BC042582-9415-4b36-9F-99-06-F1-04-C0-7C-03}</span><span class="sxs-lookup"><span data-stu-id="3b146-128">IID: {BC042582-9415-4f36-9F-99-06-F1-04-C0-7C-03}</span></span>
-   <span data-ttu-id="3b146-129">Ipmdeploymentmanager.</span><span class="sxs-lookup"><span data-stu-id="3b146-129">IPMDeploymentManager.</span></span> <span data-ttu-id="3b146-130">IID: {35F 785fa-1979-4a8b-BC-8F-FD-70-EB-0d-15-44}</span><span class="sxs-lookup"><span data-stu-id="3b146-130">IID: {35F785FA-1979-4A8B-BC-8F-FD-70-EB-0D-15-44}</span></span>
-   <span data-ttu-id="3b146-131">Ipmenumschlag Manager.</span><span class="sxs-lookup"><span data-stu-id="3b146-131">IPMEnumerationManager.</span></span> <span data-ttu-id="3b146-132">IID: {698d57c2-292d-4cf3-B7-3C-D9-5A-69-22-Ed-9a}</span><span class="sxs-lookup"><span data-stu-id="3b146-132">IID: {698D57C2-292D-4CF3-B7-3C-D9-5A-69-22-ED-9A}</span></span>
-   <span data-ttu-id="3b146-133">Ipmtaskinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-133">IPMTaskInfo.</span></span> <span data-ttu-id="3b146-134">IID: {BF1D8C33-1bf-4ee0-B5-49-6B-9d-D3-83-49-42}</span><span class="sxs-lookup"><span data-stu-id="3b146-134">IID: {BF1D8C33-1BF5-4ee0-B5-49-6B-9D-D3-83-49-42}</span></span>
-   <span data-ttu-id="3b146-135">Ipmtaskinfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-135">IPMTaskInfoEnumerator.</span></span> <span data-ttu-id="3b146-136">IID: {0630b0f 8-0bbc-4821-be-74-C7-99-51 -66-Ed-2a}</span><span class="sxs-lookup"><span data-stu-id="3b146-136">IID: {0630B0F8-0BBC-4821-BE-74-C7-99-51-66-ED-2A}</span></span>
-   <span data-ttu-id="3b146-137">Ipmextensioninfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-137">IPMExtensionInfo.</span></span> <span data-ttu-id="3b146-138">IID: {49acde 79-9788-4d0a-8a-a0-17 -46-AF-DB-9E-9d}</span><span class="sxs-lookup"><span data-stu-id="3b146-138">IID: {49ACDE79-9788-4d0a-8A-A0-17-46-AF-DB-9E-9D}</span></span>
-   <span data-ttu-id="3b146-139">Ipmextensionfileextensioninfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-139">IPMExtensionFileExtensionInfo.</span></span> <span data-ttu-id="3b146-140">IID: {6b87cb6c-0b88-4989-A4-EC-03-37-14-F7-10-D4}</span><span class="sxs-lookup"><span data-stu-id="3b146-140">IID: {6B87CB6C-0B88-4989-A4-EC-03-37-14-F7-10-D4}</span></span>
-   <span data-ttu-id="3b146-141">Ipmextensionprotocolinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-141">IPMExtensionProtocolInfo.</span></span> <span data-ttu-id="3b146-142">IID: {1e3fa036-51eb-4453-BA-FF-B8-D8-E4-B4-6C-8E}</span><span class="sxs-lookup"><span data-stu-id="3b146-142">IID: {1E3FA036-51EB-4453-BA-FF-B8-D8-E4-B4-6C-8E}</span></span>
-   <span data-ttu-id="3b146-143">Ipmextensionsharetargetinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-143">IPMExtensionShareTargetInfo.</span></span> <span data-ttu-id="3b146-144">IID: {5471b48 b-C65C-4656-8c-70-24-2E-31-19-5F-EA}</span><span class="sxs-lookup"><span data-stu-id="3b146-144">IID: {5471F48B-C65C-4656-8C-70-24-2E-31-19-5F-EA}</span></span>
-   <span data-ttu-id="3b146-145">Ipmextensionverhütungs-Info.</span><span class="sxs-lookup"><span data-stu-id="3b146-145">IPMExtensionContractInfo.</span></span> <span data-ttu-id="3b146-146">IID: {E5666373-7BA1-467c-B8-19-B1-75-dB-1C-29-5B}</span><span class="sxs-lookup"><span data-stu-id="3b146-146">IID: {E5666373-7BA1-467C-B8-19-B1-75-DB-1C-29-5B}</span></span>
-   <span data-ttu-id="3b146-147">Ipmextensionfileopenpickerinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-147">IPMExtensionFileOpenPickerInfo.</span></span> <span data-ttu-id="3b146-148">IID: {6dc91d25-9606-420c-9a-78-E0-34-a3-41-83-45}</span><span class="sxs-lookup"><span data-stu-id="3b146-148">IID: {6DC91D25-9606-420C-9A-78-E0-34-A3-41-83-45}</span></span>
-   <span data-ttu-id="3b146-149">Ipmextensionfilesavepickerinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-149">IPMExtensionFileSavePickerInfo.</span></span> <span data-ttu-id="3b146-150">IID: {38005cba-F81A-493e-a0-F8-92-2C-86-80-da-43}</span><span class="sxs-lookup"><span data-stu-id="3b146-150">IID: {38005CBA-F81A-493E-A0-F8-92-2C-86-80-DA-43}</span></span>
-   <span data-ttu-id="3b146-151">Ipmextensioncachedfileupdaterinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-151">IPMExtensionCachedFileUpdaterInfo.</span></span> <span data-ttu-id="3b146-152">IID: {E2D77509-4e58-4ba9-AF-7e-B6-42-E3-70-E1-B0}</span><span class="sxs-lookup"><span data-stu-id="3b146-152">IID: {E2D77509-4E58-4BA9-AF-7E-B6-42-E3-70-E1-B0}</span></span>
-   <span data-ttu-id="3b146-153">Ipmextensioninfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-153">IPMExtensionInfoEnumerator.</span></span> <span data-ttu-id="3b146-154">IID: {403b9e82-1171-4573-8E-6f-6f-33-F3-9B-83-DD}</span><span class="sxs-lookup"><span data-stu-id="3b146-154">IID: {403B9E82-1171-4573-8E-6F-6F-33-F3-9B-83-DD}</span></span>
-   <span data-ttu-id="3b146-155">Ipmbackgroundserviceagentinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-155">IPMBackgroundServiceAgentInfo.</span></span> <span data-ttu-id="3b146-156">IID: {3a8b46da-928c-4879-99-8c-09-DC-96-F3-D4-90}</span><span class="sxs-lookup"><span data-stu-id="3b146-156">IID: {3A8B46DA-928C-4879-99-8C-09-DC-96-F3-D4-90}</span></span>
-   <span data-ttu-id="3b146-157">Ipmbackgroundworkerinfo.</span><span class="sxs-lookup"><span data-stu-id="3b146-157">IPMBackgroundWorkerInfo.</span></span> <span data-ttu-id="3b146-158">IID: {7dd4531b-D3BF-4b6b-94-F3-69-C0-98-B1-49-7D}</span><span class="sxs-lookup"><span data-stu-id="3b146-158">IID: {7DD4531B-D3BF-4B6B-94-F3-69-C0-98-B1-49-7D}</span></span>
-   <span data-ttu-id="3b146-159">Ipmbackgroundserviceagentinfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-159">IPMBackgroundServiceAgentInfoEnumerator.</span></span> <span data-ttu-id="3b146-160">IID: {18eb2072-AB56-43b3-87-2C-be-AF-B7-A6-B3-91}</span><span class="sxs-lookup"><span data-stu-id="3b146-160">IID: {18EB2072-AB56-43B3-87-2C-BE-AF-B7-A6-B3-91}</span></span>
-   <span data-ttu-id="3b146-161">Ipmbackgroundworkerinfoenumerator.</span><span class="sxs-lookup"><span data-stu-id="3b146-161">IPMBackgroundWorkerInfoEnumerator.</span></span> <span data-ttu-id="3b146-162">IID: {87f 479f-90d8-4ec7-92-B9-72-78-7e-2F-63-6B}</span><span class="sxs-lookup"><span data-stu-id="3b146-162">IID: {87F479F8-90D8-4EC7-92-B9-72-78-7E-2F-63-6B}</span></span>

 

 




