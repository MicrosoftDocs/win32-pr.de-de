---
description: Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Abfragen oder Ändern der Datenbank der installierten Dienste verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Konfigurieren eines Dienstanbieter mit SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348970"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="ca17f-105">Konfigurieren eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="ca17f-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="ca17f-106">Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Abfragen oder Ändern der Datenbank der installierten Dienste verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca17f-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="ca17f-107">Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ca17f-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="ca17f-108">Die Syntax lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="ca17f-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca17f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca17f-109">Syntax</span></span>

<span data-ttu-id="ca17f-110">**SC** \[ *Servername* \] *Befehl* \[ *Dienst Name* \] \[  \] Option1 \[ *Option2* \] ...</span><span class="sxs-lookup"><span data-stu-id="ca17f-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="ca17f-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Servername*</span><span class="sxs-lookup"><span data-stu-id="ca17f-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="ca17f-112">Optionaler Servername.</span><span class="sxs-lookup"><span data-stu-id="ca17f-112">Optional server name.</span></span> <span data-ttu-id="ca17f-113">Verwenden Sie das Formular \\ \\ *Servername*.</span><span class="sxs-lookup"><span data-stu-id="ca17f-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="ca17f-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*S*</span><span class="sxs-lookup"><span data-stu-id="ca17f-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="ca17f-115">Einer der folgenden Befehle:</span><span class="sxs-lookup"><span data-stu-id="ca17f-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="ca17f-116">starten</span><span class="sxs-lookup"><span data-stu-id="ca17f-116">boot</span></span></dd> <dd><span data-ttu-id="ca17f-117">config</span><span class="sxs-lookup"><span data-stu-id="ca17f-117">config</span></span></dd> <dd><span data-ttu-id="ca17f-118">create</span><span class="sxs-lookup"><span data-stu-id="ca17f-118">create</span></span></dd> <dd><span data-ttu-id="ca17f-119">delete</span><span class="sxs-lookup"><span data-stu-id="ca17f-119">delete</span></span></dd> <dd><span data-ttu-id="ca17f-120">description</span><span class="sxs-lookup"><span data-stu-id="ca17f-120">description</span></span></dd> <dd><span data-ttu-id="ca17f-121">Enumabhängig</span><span class="sxs-lookup"><span data-stu-id="ca17f-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="ca17f-122">failure</span><span class="sxs-lookup"><span data-stu-id="ca17f-122">failure</span></span></dd> <dd><span data-ttu-id="ca17f-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="ca17f-123">failureflag</span></span></dd> <dd><span data-ttu-id="ca17f-124">GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="ca17f-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="ca17f-125">Getkeyname</span><span class="sxs-lookup"><span data-stu-id="ca17f-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="ca17f-126">Sperre</span><span class="sxs-lookup"><span data-stu-id="ca17f-126">Lock</span></span></dd> <dd><span data-ttu-id="ca17f-127">qc</span><span class="sxs-lookup"><span data-stu-id="ca17f-127">qc</span></span></dd> <dd><span data-ttu-id="ca17f-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="ca17f-128">qdescription</span></span></dd> <dd><span data-ttu-id="ca17f-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="ca17f-129">qfailure</span></span></dd> <dd><span data-ttu-id="ca17f-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="ca17f-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="ca17f-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="ca17f-131">qprivs</span></span></dd> <dd><span data-ttu-id="ca17f-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="ca17f-132">qsidtype</span></span></dd> <dd><span data-ttu-id="ca17f-133">Abfrage</span><span class="sxs-lookup"><span data-stu-id="ca17f-133">query</span></span></dd> <dd><span data-ttu-id="ca17f-134">QUERYEX</span><span class="sxs-lookup"><span data-stu-id="ca17f-134">queryex</span></span></dd> <dd><span data-ttu-id="ca17f-135">privs</span><span class="sxs-lookup"><span data-stu-id="ca17f-135">privs</span></span></dd> <dd><span data-ttu-id="ca17f-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="ca17f-136">QueryLock</span></span></dd> <dd><span data-ttu-id="ca17f-137">Sdset</span><span class="sxs-lookup"><span data-stu-id="ca17f-137">sdset</span></span></dd> <dd><span data-ttu-id="ca17f-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="ca17f-138">sdshow</span></span></dd> <dd><span data-ttu-id="ca17f-139">showsid</span><span class="sxs-lookup"><span data-stu-id="ca17f-139">showsid</span></span></dd> <dd><span data-ttu-id="ca17f-140">SIDType</span><span class="sxs-lookup"><span data-stu-id="ca17f-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="ca17f-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Service Name*</span><span class="sxs-lookup"><span data-stu-id="ca17f-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="ca17f-142">Der Name des Dienstanbieter, der bei der Installation angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ca17f-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="ca17f-143"><span id="option1"></span><span id="OPTION1"></span>*Option1*</span><span class="sxs-lookup"><span data-stu-id="ca17f-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="ca17f-144">Ein optionaler Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca17f-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ca17f-145"><span id="option2"></span><span id="OPTION2"></span>*Option2*</span><span class="sxs-lookup"><span data-stu-id="ca17f-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="ca17f-146">Ein optionaler Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca17f-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca17f-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca17f-147">Remarks</span></span>

<span data-ttu-id="ca17f-148">Verwenden Sie den folgenden Befehl, um die umfassende Syntax für einen Befehl anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="ca17f-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="ca17f-149">**SC** - *Befehl*</span><span class="sxs-lookup"><span data-stu-id="ca17f-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca17f-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca17f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca17f-151">Dienstkonfiguration:</span><span class="sxs-lookup"><span data-stu-id="ca17f-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="ca17f-152">Dienst Installation, Entfernung und Enumeration</span><span class="sxs-lookup"><span data-stu-id="ca17f-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



