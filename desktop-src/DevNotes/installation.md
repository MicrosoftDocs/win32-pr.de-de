---
description: Installation
ms.assetid: 02A7866F-0F72-4437-A882-EEE9C2E28EC7
title: Installation (Entwickler Hinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ddb476b6688bbbbef27eab571e3219071656a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861447"
---
# <a name="installation-developer-notes"></a><span data-ttu-id="4ffa9-103">Installation (Entwickler Hinweise)</span><span class="sxs-lookup"><span data-stu-id="4ffa9-103">Installation (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ffa9-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4ffa9-104">In this section</span></span>

-   [<span data-ttu-id="4ffa9-105">**Coinstall**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-105">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
-   [<span data-ttu-id="4ffa9-106">**Iceginstallinetcomponents**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-106">**IcfgInstallInetComponents**</span></span>](icfginstallinetcomponents.md)
-   [<span data-ttu-id="4ffa9-107">**Icegneedinetcomponents**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-107">**IcfgNeedInetComponents**</span></span>](icfgneedinetcomponents.md)
-   [<span data-ttu-id="4ffa9-108">**Installcatalog**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-108">**InstallCatalog**</span></span>](installcatalog.md)
-   [<span data-ttu-id="4ffa9-109">**Installcomponentw**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-109">**InstallComponentW**</span></span>](installcomponentw.md)
-   [<span data-ttu-id="4ffa9-110">**Installperfdll**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-110">**InstallPerfDll**</span></span>](/windows/desktop/api/LoadPerf/nf-loadperf-installperfdlla)
-   [<span data-ttu-id="4ffa9-111">**LoadLibraryShim**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-111">**LoadLibraryShim**</span></span>](loadlibraryshim.md)
-   [<span data-ttu-id="4ffa9-112">**Ocinitialize**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-112">**OcInitialize**</span></span>](ocinitialize.md)
-   [<span data-ttu-id="4ffa9-113">**Okbeenden**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-113">**OcTerminate**</span></span>](octerminate.md)
-   [<span data-ttu-id="4ffa9-114">**psetupgetfiletitle**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-114">**pSetupGetFileTitle**</span></span>](psetupgetfiletitle.md)
-   [<span data-ttu-id="4ffa9-115">**psetupgetglobalflags**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-115">**pSetupGetGlobalFlags**</span></span>](psetupgetglobalflags.md)
-   [<span data-ttu-id="4ffa9-116">**psetupinstallcatalog**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-116">**pSetupInstallCatalog**</span></span>](psetupinstallcatalog.md)
-   [<span data-ttu-id="4ffa9-117">**psetupisuseradmin**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-117">**pSetupIsUserAdmin**</span></span>](psetupisuseradmin.md)
-   [<span data-ttu-id="4ffa9-118">**psetupsetglobalflags**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-118">**pSetupSetGlobalFlags**</span></span>](psetupsetglobalflags.md)
-   [<span data-ttu-id="4ffa9-119">**psetupstringtabledestroy**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-119">**pSetupStringTableDestroy**</span></span>](psetupstringtabledestroy.md)
-   [<span data-ttu-id="4ffa9-120">**psetupstringtableaddstringex**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-120">**pSetupStringTableAddStringEx**</span></span>](psetupstringtableaddstringex.md)
-   [<span data-ttu-id="4ffa9-121">**psetupstringtableinitializeex**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-121">**pSetupStringTableInitializeEx**</span></span>](psetupstringtableinitializeex.md)
-   [<span data-ttu-id="4ffa9-122">**psetupstringtableinitialize**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-122">**pSetupStringTableInitialize**</span></span>](psetupstringtableinitialize.md)
-   [<span data-ttu-id="4ffa9-123">**psetupverifycatalogfile**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-123">**pSetupVerifyCatalogFile**</span></span>](psetupverifycatalogfile.md)
-   [<span data-ttu-id="4ffa9-124">**Konfiguration erneut laden \_**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-124">**reload\_config**</span></span>](reload-config.md)
-   [<span data-ttu-id="4ffa9-125">**Sxslookupclrguid**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-125">**SxsLookupClrGuid**</span></span>](sxslookupclrguid.md)
-   [<span data-ttu-id="4ffa9-126">**Uninstallcomponent**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-126">**UninstallComponent**</span></span>](uninstallcomponent.md)
-   [<span data-ttu-id="4ffa9-127">**Verifycatalogfile**</span><span class="sxs-lookup"><span data-stu-id="4ffa9-127">**VerifyCatalogFile**</span></span>](verifycatalogfile.md)

 

 
