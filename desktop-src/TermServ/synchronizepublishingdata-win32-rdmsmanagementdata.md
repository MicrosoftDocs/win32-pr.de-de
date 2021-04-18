---
title: Synchronizepublishingdata-Methode der Win32_RDMSManagementData-Klasse
description: Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Synchronizepublishingdata-Methode Remotedesktopdienste
- Synchronizepublishingdata-Methode Remotedesktopdienste, Win32_RDMSManagementData-Klasse
- Win32_RDMSManagementData-Klasse Remotedesktopdienste, synchronizepublishingdata-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391861"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="588d9-106">Synchronizepublishingdata-Methode der Win32 \_ rdmsmanagementdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="588d9-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="588d9-107">Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).</span><span class="sxs-lookup"><span data-stu-id="588d9-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="588d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="588d9-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="588d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="588d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588d9-110">*Kontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="588d9-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588d9-111">Die Kontextinformationen der zu synchronisierenden Veröffentlichungsdaten.</span><span class="sxs-lookup"><span data-stu-id="588d9-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588d9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="588d9-112">Return value</span></span>

<span data-ttu-id="588d9-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="588d9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="588d9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="588d9-114">Requirements</span></span>



| <span data-ttu-id="588d9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="588d9-115">Requirement</span></span> | <span data-ttu-id="588d9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="588d9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="588d9-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="588d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="588d9-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="588d9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="588d9-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="588d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="588d9-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="588d9-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="588d9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="588d9-121">Namespace</span></span><br/>                | <span data-ttu-id="588d9-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="588d9-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="588d9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="588d9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="588d9-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="588d9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="588d9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="588d9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="588d9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="588d9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="588d9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="588d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588d9-128">**Win32 \_ rdmsmanagementdata**</span><span class="sxs-lookup"><span data-stu-id="588d9-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





