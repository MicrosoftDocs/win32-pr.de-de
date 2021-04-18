---
title: Win32_RDMSEnvironment-Klasse
description: Verwaltet eine RDMs-Umgebung (Remotedesktop Management Services).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste
- Win32_RDMSEnvironment Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339560"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="6ec47-105">Win32 \_ rdmsenvironment-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ec47-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="6ec47-106">Verwaltet eine RDMs-Umgebung (Remotedesktop Management Services).</span><span class="sxs-lookup"><span data-stu-id="6ec47-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="6ec47-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ec47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ec47-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="6ec47-109">Member</span><span class="sxs-lookup"><span data-stu-id="6ec47-109">Members</span></span>

<span data-ttu-id="6ec47-110">Die **Win32 \_ rdmsenvironment** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6ec47-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="6ec47-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ec47-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ec47-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ec47-112">Methods</span></span>

<span data-ttu-id="6ec47-113">Die **Win32 \_ rdmsenvironment** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ec47-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="6ec47-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6ec47-114">Method</span></span>                                                                   | <span data-ttu-id="6ec47-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec47-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ec47-116">**Getactiveserver**</span><span class="sxs-lookup"><span data-stu-id="6ec47-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="6ec47-117">Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="6ec47-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="6ec47-118">**Getclientaccessname**</span><span class="sxs-lookup"><span data-stu-id="6ec47-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="6ec47-119">Ruft den Namen der RDMs-Umgebung des Domain Name System (DNS)-Ressourceneinsatzes (RR) ab.</span><span class="sxs-lookup"><span data-stu-id="6ec47-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="6ec47-120">**"Abtactiveserver"**</span><span class="sxs-lookup"><span data-stu-id="6ec47-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="6ec47-121">Legt den FQDN der RDMs-Umgebung auf den aktuellen Knoten fest.</span><span class="sxs-lookup"><span data-stu-id="6ec47-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="6ec47-122">**Setclientaccessname**</span><span class="sxs-lookup"><span data-stu-id="6ec47-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="6ec47-123">Aktualisiert den DNS-RR-Namen der RDMs-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6ec47-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="6ec47-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ec47-124">Requirements</span></span>



| <span data-ttu-id="6ec47-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ec47-125">Requirement</span></span> | <span data-ttu-id="6ec47-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6ec47-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec47-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ec47-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec47-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ec47-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6ec47-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ec47-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec47-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ec47-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6ec47-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ec47-131">Namespace</span></span><br/>                | <span data-ttu-id="6ec47-132">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="6ec47-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6ec47-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec47-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec47-134"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ec47-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec47-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec47-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec47-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec47-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6ec47-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ec47-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec47-138">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6ec47-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





