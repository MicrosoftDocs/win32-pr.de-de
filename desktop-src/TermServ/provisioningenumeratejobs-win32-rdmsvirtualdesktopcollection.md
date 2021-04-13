---
title: Provisioningenenumeratejobs-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Provisioningenumschlag-Methode Remotedesktopdienste
- Provisioningenenumeratejobs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningenenumeratejobs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518998"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="45cc3-106">Provisioningenumeratejobs-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="45cc3-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="45cc3-107">Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.</span><span class="sxs-lookup"><span data-stu-id="45cc3-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cc3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="45cc3-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="45cc3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="45cc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45cc3-110">*JobType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45cc3-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cc3-111">Eine ganze Zahl, die den Typ des aufzuzählenden Auftrags angibt.</span><span class="sxs-lookup"><span data-stu-id="45cc3-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="45cc3-112">Dieser Parameter kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="45cc3-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="45cc3-113">0</span><span class="sxs-lookup"><span data-stu-id="45cc3-113">0</span></span>
</dt> <dd>

<span data-ttu-id="45cc3-114">Ausführen von Aufträgen</span><span class="sxs-lookup"><span data-stu-id="45cc3-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="45cc3-115">1</span><span class="sxs-lookup"><span data-stu-id="45cc3-115">1</span></span>
</dt> <dd>

<span data-ttu-id="45cc3-116">Abgeschlossene Aufträge</span><span class="sxs-lookup"><span data-stu-id="45cc3-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="45cc3-117">*Collectionalias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45cc3-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45cc3-118">Der Alias der aufzuzählenden Auflistung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="45cc3-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="45cc3-119">Der Standardwert für diesen Parameter ist false. er gibt an, dass alle ausgeführte Aufträge aufgezählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45cc3-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="45cc3-120">*Jobguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45cc3-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45cc3-121">Ein Array, das die **GUIDs** der aufzuzählenden Bereitstellungs Aufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="45cc3-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45cc3-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45cc3-122">Return value</span></span>

<span data-ttu-id="45cc3-123">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45cc3-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="45cc3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45cc3-124">Requirements</span></span>



| <span data-ttu-id="45cc3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45cc3-125">Requirement</span></span> | <span data-ttu-id="45cc3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="45cc3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cc3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45cc3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45cc3-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="45cc3-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="45cc3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45cc3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45cc3-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45cc3-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="45cc3-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="45cc3-131">Namespace</span></span><br/>                | <span data-ttu-id="45cc3-132">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="45cc3-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="45cc3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="45cc3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45cc3-134"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45cc3-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="45cc3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="45cc3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cc3-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45cc3-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="45cc3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45cc3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cc3-138">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="45cc3-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





