---
description: Die IWbemClassObject-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: IWbemClassObject-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350088"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="ad787-103">IWbemClassObject-Methoden</span><span class="sxs-lookup"><span data-stu-id="ad787-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="ad787-104">Die [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad787-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ad787-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ad787-105">In this section</span></span>

-   [<span data-ttu-id="ad787-106">**Beginenumeration-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="ad787-107">**Beginmethodenumeration-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="ad787-108">**Clone-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="ad787-109">**CompareTo-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="ad787-110">**Delete-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="ad787-111">**DeleteMethod-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="ad787-112">**Umeration-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="ad787-113">**Endmethodenumeration-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="ad787-114">**Get-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="ad787-115">**GetMethod-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="ad787-116">**Getmethodorigin-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="ad787-117">**Getmethodqualifierset-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="ad787-118">**GetNames-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="ad787-119">**Getobjecttext-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="ad787-120">**Getpropertyorigin-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="ad787-121">**Getpropertyqualifierset-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="ad787-122">**Getqualifierset-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="ad787-123">**Verersfrom-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="ad787-124">**Nächste Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="ad787-125">**Nextmethod-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="ad787-126">**Put-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="ad787-127">**Putmethod-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="ad787-128">**Spawnderivedclass-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="ad787-129">**SpawnInstance-Methode**</span><span class="sxs-lookup"><span data-stu-id="ad787-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



