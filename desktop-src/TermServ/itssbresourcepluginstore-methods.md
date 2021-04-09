---
title: Itssbresourcepluginstore-Methoden
description: Die itssbresourcepluginstore-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856407"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="edb1f-103">Itssbresourcepluginstore-Methoden</span><span class="sxs-lookup"><span data-stu-id="edb1f-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="edb1f-104">Die [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="edb1f-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="edb1f-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="edb1f-105">In this section</span></span>

-   [<span data-ttu-id="edb1f-106">**Acquiretargetlock-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="edb1f-107">**Addenvironmentdestore-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="edb1f-108">**Addsessiondestore-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="edb1f-109">**Addtargetdestore-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="edb1f-110">**DeleteTarget-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="edb1f-111">**Enumerateenvironment-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="edb1f-112">**Enumeratefarms-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="edb1f-113">**Enumeratesessions-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="edb1f-114">**Enumeratetargets-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="edb1f-115">**Getfarmproperty-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="edb1f-116">**Getserverstate-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="edb1f-117">**Queryenvironment-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="edb1f-118">**Querysessionbysessionid-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="edb1f-119">**Querytarget-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="edb1f-120">**Releasetargetlock-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="edb1f-121">**Removeumgebfromstore-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="edb1f-122">**Saveenvironment-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="edb1f-123">**Savesession-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="edb1f-124">**Savetarget-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="edb1f-125">**Die Methode "stenvironmentproperty"**</span><span class="sxs-lookup"><span data-stu-id="edb1f-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="edb1f-126">**Methode "" der Methode ""**</span><span class="sxs-lookup"><span data-stu-id="edb1f-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="edb1f-127">**Setserverdrainmode-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="edb1f-128">**Setserverwaitingdestart-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="edb1f-129">**Die Methode "endessionstate"**</span><span class="sxs-lookup"><span data-stu-id="edb1f-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="edb1f-130">**SetTargetProperty-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="edb1f-131">**Settargetpropertywithversioncheck-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="edb1f-132">**Settargetstate-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="edb1f-133">**Testandsetserverstate-Methode**</span><span class="sxs-lookup"><span data-stu-id="edb1f-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




