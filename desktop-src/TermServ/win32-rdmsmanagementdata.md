---
title: Win32_RDMSManagementData-Klasse
description: Synchronisiert Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData-Klasse Remotedesktopdienste
- Win32_RDMSManagementData Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040200"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="f82fd-105">Win32 \_ rdmsmanagementdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="f82fd-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="f82fd-106">Synchronisiert Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).</span><span class="sxs-lookup"><span data-stu-id="f82fd-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="f82fd-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f82fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f82fd-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="f82fd-109">Member</span><span class="sxs-lookup"><span data-stu-id="f82fd-109">Members</span></span>

<span data-ttu-id="f82fd-110">Die **Win32 \_ rdmsmanagementdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f82fd-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="f82fd-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f82fd-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f82fd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f82fd-112">Methods</span></span>

<span data-ttu-id="f82fd-113">Die **Win32 \_ rdmsmanagementdata** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f82fd-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="f82fd-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f82fd-114">Method</span></span>                                                                                        | <span data-ttu-id="f82fd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f82fd-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="f82fd-116">**Synchronizeallpublishingdata**</span><span class="sxs-lookup"><span data-stu-id="f82fd-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="f82fd-117">Synchronisiert alle Veröffentlichungsdaten für RDMs.</span><span class="sxs-lookup"><span data-stu-id="f82fd-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="f82fd-118">**Synchronizepublishingdata**</span><span class="sxs-lookup"><span data-stu-id="f82fd-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="f82fd-119">Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für RDMs.</span><span class="sxs-lookup"><span data-stu-id="f82fd-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f82fd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f82fd-120">Requirements</span></span>



| <span data-ttu-id="f82fd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f82fd-121">Requirement</span></span> | <span data-ttu-id="f82fd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f82fd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f82fd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f82fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f82fd-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f82fd-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f82fd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f82fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f82fd-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f82fd-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f82fd-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f82fd-127">Namespace</span></span><br/>                | <span data-ttu-id="f82fd-128">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="f82fd-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f82fd-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f82fd-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f82fd-130"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f82fd-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f82fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f82fd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f82fd-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f82fd-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f82fd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f82fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f82fd-134">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f82fd-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





