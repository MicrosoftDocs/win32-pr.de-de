---
title: Funktionen des RAS-Diensts
description: Verwenden Sie die folgenden Funktionen, um RAS-Funktionen zu implementieren.
ms.assetid: 5883a77a-6af8-47a8-bb28-6ef60a5aa2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d272403c8cd485f5e9d3d1de0c7fe5ac1cac9442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102131"
---
# <a name="remote-access-service-functions"></a><span data-ttu-id="ca7b4-103">Funktionen des RAS-Diensts</span><span class="sxs-lookup"><span data-stu-id="ca7b4-103">Remote Access Service Functions</span></span>

<span data-ttu-id="ca7b4-104">Verwenden Sie die folgenden Funktionen, um RAS-Funktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ca7b4-104">Use the following functions to implement RAS functionality.</span></span>

<span data-ttu-id="ca7b4-105">**Cmfree**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-105">**CmFree**</span></span>

<span data-ttu-id="ca7b4-106">**Cmmzuweisung**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-106">**CmMalloc**</span></span>

[<span data-ttu-id="ca7b4-107">**Orasadfunc**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-107">**ORASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-orasadfunc)

[<span data-ttu-id="ca7b4-108">**Rasadfunc**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-108">**RASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasadfunca)

[<span data-ttu-id="ca7b4-109">**Rasclearconnectionstatistics**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-109">**RasClearConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearconnectionstatistics)

[<span data-ttu-id="ca7b4-110">**Rasclearlinkstatistics**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-110">**RasClearLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearlinkstatistics)

[<span data-ttu-id="ca7b4-111">**Rasconnectionnotification**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-111">**RasConnectionNotification**</span></span>](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)

[<span data-ttu-id="ca7b4-112">**Rascreatephonebookentry**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-112">**RasCreatePhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya)

[<span data-ttu-id="ca7b4-113">**Rascustomdeleteentrynotify**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-113">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

[<span data-ttu-id="ca7b4-114">**Rascustomdial**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-114">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)

[<span data-ttu-id="ca7b4-115">**Rascustomdialdlg**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-115">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)

[<span data-ttu-id="ca7b4-116">**Rascustomentrydlg**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-116">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)

[<span data-ttu-id="ca7b4-117">**Rascustomhangup**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-117">**RasCustomHangUp**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)

[<span data-ttu-id="ca7b4-118">**Rasdeleteentry**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-118">**RasDeleteEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya)

[<span data-ttu-id="ca7b4-119">**Rasdelta etesubentry**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-119">**RasDeleteSubEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeletesubentrya)

[<span data-ttu-id="ca7b4-120">**Rasdial**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-120">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)

[<span data-ttu-id="ca7b4-121">**RasDialDlg**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-121">**RasDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)

[<span data-ttu-id="ca7b4-122">**Rasdialfunc**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-122">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)

[<span data-ttu-id="ca7b4-123">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-123">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)

[<span data-ttu-id="ca7b4-124">**RasDialFunc2**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-124">**RasDialFunc2**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc2)

[<span data-ttu-id="ca7b4-125">**Raseditphonebookentry**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-125">**RasEditPhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya)

[<span data-ttu-id="ca7b4-126">**RasEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-126">**RasEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)

[<span data-ttu-id="ca7b4-127">**Rasen-autodialadressen**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-127">**RasEnumAutodialAddresses**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa)

[<span data-ttu-id="ca7b4-128">**Rasen-Connections**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-128">**RasEnumConnections**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)

[<span data-ttu-id="ca7b4-129">**Rasengeräte**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-129">**RasEnumDevices**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)

[<span data-ttu-id="ca7b4-130">**Raseneinträge**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-130">**RasEnumEntries**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)

[<span data-ttu-id="ca7b4-131">**Rasfreeapuseridentity**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-131">**RasFreeEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasfreeeapuseridentitya)

[<span data-ttu-id="ca7b4-132">**Rasgetautodialaddress**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-132">**RasGetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa)

[<span data-ttu-id="ca7b4-133">**Rasgetautodialenable**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-133">**RasGetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea)

[<span data-ttu-id="ca7b4-134">**Rasgetautodialparam**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-134">**RasGetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama)

[<span data-ttu-id="ca7b4-135">**"Rasgetconnectionstatistics"**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-135">**RasGetConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectionstatistics)

[<span data-ttu-id="ca7b4-136">**Rasgetconnectstatus**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-136">**RasGetConnectStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)

[<span data-ttu-id="ca7b4-137">**Rasgetcountryinfo**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-137">**RasGetCountryInfo**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa)

[<span data-ttu-id="ca7b4-138">**Rasgetanmeldeinformationen**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-138">**RasGetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa)

[<span data-ttu-id="ca7b4-139">**Rasgetcustomauthdata**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-139">**RasGetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcustomauthdataa)

[<span data-ttu-id="ca7b4-140">**Rasgeteapuserdata**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-140">**RasGetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuserdataa)

[<span data-ttu-id="ca7b4-141">**Rasgeteapuseridentity**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-141">**RasGetEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuseridentitya)

[<span data-ttu-id="ca7b4-142">**Rasgetentrydialparameams**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-142">**RasGetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa)

[<span data-ttu-id="ca7b4-143">**Rasgetentryproperties**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-143">**RasGetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)

[<span data-ttu-id="ca7b4-144">**Rasgeterrorstring**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-144">**RasGetErrorString**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)

[<span data-ttu-id="ca7b4-145">**"Rasgetlinkstatistics"**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-145">**RasGetLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetlinkstatistics)

[<span data-ttu-id="ca7b4-146">**Rasgetnapstatus**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-146">**RasGetNapStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetnapstatus)

<span data-ttu-id="ca7b4-147">[**Rasgetprojectioninfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ca7b4-147">[**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span></span>

[<span data-ttu-id="ca7b4-148">**Rasgetprojectioninfoex**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-148">**RasGetProjectionInfoEx**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetprojectioninfoex)

<span data-ttu-id="ca7b4-149">[**Rasgetquarantineconnectionid**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca7b4-149">[**RasGetQuarantineConnectionId**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span></span>

[<span data-ttu-id="ca7b4-150">**Rasgetsubentryhandle**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-150">**RasGetSubEntryHandle**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea)

[<span data-ttu-id="ca7b4-151">**Rasgetsubentryproperties**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-151">**RasGetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa)

[<span data-ttu-id="ca7b4-152">**RasHangUp**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-152">**RasHangUp**</span></span>](/windows/desktop/api/Ras/nf-ras-rashangupa)

[<span data-ttu-id="ca7b4-153">**Rasinvokeeapui**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-153">**RasInvokeEapUI**</span></span>](/windows/desktop/api/Ras/nf-ras-rasinvokeeapui)

<span data-ttu-id="ca7b4-154">[**Rasmonitordlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca7b4-154">[**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span></span>

[<span data-ttu-id="ca7b4-155">**Raspbdlgfunc**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-155">**RasPBDlgFunc**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca)

[<span data-ttu-id="ca7b4-156">**Rasphonebookdlg**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-156">**RasPhonebookDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga)

[<span data-ttu-id="ca7b4-157">**Rasrenameentry**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-157">**RasRenameEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasrenameentrya)

[<span data-ttu-id="ca7b4-158">**Rassetauwebdialaddress**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-158">**RasSetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa)

[<span data-ttu-id="ca7b4-159">**Rassetauto dialenable**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-159">**RasSetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea)

[<span data-ttu-id="ca7b4-160">**Rassetauto dialparam**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-160">**RasSetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialparama)

[<span data-ttu-id="ca7b4-161">**Rassetcommsettings**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-161">**RasSetCommSettings**</span></span>](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings)

[<span data-ttu-id="ca7b4-162">**Rassetanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-162">**RasSetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa)

[<span data-ttu-id="ca7b4-163">**Rassetcustomauthdata**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-163">**RasSetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcustomauthdataa)

[<span data-ttu-id="ca7b4-164">**Rasseteapuserdata**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-164">**RasSetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasseteapuserdataa)

[<span data-ttu-id="ca7b4-165">**Rassetentrydialparametriams**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-165">**RasSetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa)

[<span data-ttu-id="ca7b4-166">**Rassetentryproperties**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-166">**RasSetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa)

[<span data-ttu-id="ca7b4-167">**Rassetsubentryproperties**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-167">**RasSetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)

[<span data-ttu-id="ca7b4-168">**Rasupdateconnetction**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-168">**RasUpdateConnection**</span></span>](/windows/desktop/api/Ras/nf-ras-rasupdateconnection)

[<span data-ttu-id="ca7b4-169">**Rasvalidateentryname**</span><span class="sxs-lookup"><span data-stu-id="ca7b4-169">**RasValidateEntryName**</span></span>](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea)

[<span data-ttu-id="ca7b4-170">Benutzerdefinierte RAS-DLL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ca7b4-170">RAS Custom Scripting DLL Functions</span></span>](ras-custom-scripting-dll-functions.md)

 

 