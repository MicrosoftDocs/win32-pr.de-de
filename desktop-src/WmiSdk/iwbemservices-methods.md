---
description: Die IWbemServices-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: IWbemServices-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349272"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="de4dc-103">IWbemServices-Methoden</span><span class="sxs-lookup"><span data-stu-id="de4dc-103">IWbemServices Methods</span></span>

<span data-ttu-id="de4dc-104">Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="de4dc-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de4dc-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="de4dc-105">In this section</span></span>

-   [<span data-ttu-id="de4dc-106">**Cancelasynccall-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="de4dc-107">**Methode "kreateclassenum"**</span><span class="sxs-lookup"><span data-stu-id="de4dc-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="de4dc-108">**Methode "kreateclassenumschlag"**</span><span class="sxs-lookup"><span data-stu-id="de4dc-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="de4dc-109">**Methode "kreateinstanceaufumum"**</span><span class="sxs-lookup"><span data-stu-id="de4dc-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="de4dc-110">**Methode "kreateingestanceenumasync"**</span><span class="sxs-lookup"><span data-stu-id="de4dc-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="de4dc-111">**Deleteclass-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="de4dc-112">**DeleteClassAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="de4dc-113">**Delta einstance-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="de4dc-114">**Delta einstanceasync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="de4dc-115">**ExecMethod-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="de4dc-116">**ExecMethodAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="de4dc-117">**ExecNotificationQuery-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="de4dc-118">**ExecNotificationQueryAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="de4dc-119">**ExecQuery-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="de4dc-120">**ExecQueryAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="de4dc-121">**GetObject-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="de4dc-122">**GetObjectAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="de4dc-123">**OpenNamespace-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="de4dc-124">**Putclass-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="de4dc-125">**PutClassAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="de4dc-126">**PutInstance-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="de4dc-127">**PutInstanceAsync-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="de4dc-128">**Queryobjectsink-Methode**</span><span class="sxs-lookup"><span data-stu-id="de4dc-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 



