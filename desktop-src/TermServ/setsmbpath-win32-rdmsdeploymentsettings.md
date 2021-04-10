---
title: Setsmbpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert den UNC-Pfad zur SMB-Freigabe, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Setsmbpath-Methode Remotedesktopdienste
- Setsmbpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setsmbpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956748"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7834c-106">Setsmbpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="7834c-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7834c-107">Aktualisiert den UNC-Pfad zur SMB-Freigabe, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7834c-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7834c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7834c-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="7834c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7834c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7834c-110">*Directoriypath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7834c-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7834c-111">Der neue Pfad zur SMB-Freigabe im UNC-Format.</span><span class="sxs-lookup"><span data-stu-id="7834c-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7834c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7834c-112">Return value</span></span>

<span data-ttu-id="7834c-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7834c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7834c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7834c-114">Requirements</span></span>



| <span data-ttu-id="7834c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7834c-115">Requirement</span></span> | <span data-ttu-id="7834c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7834c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7834c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7834c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7834c-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7834c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7834c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7834c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7834c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7834c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7834c-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7834c-121">Namespace</span></span><br/>                | <span data-ttu-id="7834c-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="7834c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7834c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7834c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7834c-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7834c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7834c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7834c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7834c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7834c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7834c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7834c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7834c-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="7834c-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





