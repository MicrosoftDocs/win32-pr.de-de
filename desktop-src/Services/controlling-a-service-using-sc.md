---
description: Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Steuern eines Dienstanbieter verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Steuern eines Dienstanbieter mit SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359462"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="6cd48-105">Steuern eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="6cd48-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="6cd48-106">Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Steuern eines Dienstanbieter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6cd48-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="6cd48-107">Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6cd48-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="6cd48-108">Die Syntax lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="6cd48-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd48-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cd48-109">Syntax</span></span>

<span data-ttu-id="6cd48-110">**SC** \[ *Servername* \] *Befehl* \[ *Dienst Name* \] \[  \] Option1 \[ *Option2* \] ...</span><span class="sxs-lookup"><span data-stu-id="6cd48-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="6cd48-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Servername*</span><span class="sxs-lookup"><span data-stu-id="6cd48-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="6cd48-112">Optionaler Servername.</span><span class="sxs-lookup"><span data-stu-id="6cd48-112">Optional server name.</span></span> <span data-ttu-id="6cd48-113">Verwenden Sie das Formular \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="6cd48-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="6cd48-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*S*</span><span class="sxs-lookup"><span data-stu-id="6cd48-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="6cd48-115">Einer der folgenden Befehle:</span><span class="sxs-lookup"><span data-stu-id="6cd48-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="6cd48-116">continue</span><span class="sxs-lookup"><span data-stu-id="6cd48-116">continue</span></span></dd> <dd><span data-ttu-id="6cd48-117">Steuerung</span><span class="sxs-lookup"><span data-stu-id="6cd48-117">control</span></span></dd> <dd><span data-ttu-id="6cd48-118">abzufragen</span><span class="sxs-lookup"><span data-stu-id="6cd48-118">interrogate</span></span></dd> <dd><span data-ttu-id="6cd48-119">pause</span><span class="sxs-lookup"><span data-stu-id="6cd48-119">pause</span></span></dd> <dd><span data-ttu-id="6cd48-120">start</span><span class="sxs-lookup"><span data-stu-id="6cd48-120">start</span></span></dd> <dd><span data-ttu-id="6cd48-121">stop</span><span class="sxs-lookup"><span data-stu-id="6cd48-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="6cd48-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Service Name*</span><span class="sxs-lookup"><span data-stu-id="6cd48-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="6cd48-123">Der Name des Dienstanbieter, der bei der Installation angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6cd48-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="6cd48-124"><span id="option1"></span><span id="OPTION1"></span>*Option1*</span><span class="sxs-lookup"><span data-stu-id="6cd48-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="6cd48-125">Ein optionaler Parameter.</span><span class="sxs-lookup"><span data-stu-id="6cd48-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6cd48-126"><span id="option2"></span><span id="OPTION2"></span>*Option2*</span><span class="sxs-lookup"><span data-stu-id="6cd48-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="6cd48-127">Ein optionaler Parameter.</span><span class="sxs-lookup"><span data-stu-id="6cd48-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cd48-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cd48-128">Remarks</span></span>

<span data-ttu-id="6cd48-129">Verwenden Sie den folgenden Befehl, um die umfassende Syntax für einen Befehl anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="6cd48-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="6cd48-130">**SC** - *Befehl*</span><span class="sxs-lookup"><span data-stu-id="6cd48-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cd48-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cd48-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cd48-132">Dienst Steuerungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="6cd48-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="6cd48-133">Dienst Start</span><span class="sxs-lookup"><span data-stu-id="6cd48-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



