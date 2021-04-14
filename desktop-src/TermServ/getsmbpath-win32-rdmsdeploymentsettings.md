---
title: Getsmbpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Getsmbpath-Methode Remotedesktopdienste
- Getsmbpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getsmbpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392228"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="19aa5-106">Getsmbpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="19aa5-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="19aa5-107">Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="19aa5-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="19aa5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19aa5-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="19aa5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19aa5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19aa5-110">*Directoriypath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19aa5-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19aa5-111">Empfängt einen UNC-formatierten Pfad zur SMB-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="19aa5-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19aa5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19aa5-112">Return value</span></span>

<span data-ttu-id="19aa5-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19aa5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19aa5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19aa5-114">Requirements</span></span>



| <span data-ttu-id="19aa5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19aa5-115">Requirement</span></span> | <span data-ttu-id="19aa5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="19aa5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="19aa5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19aa5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19aa5-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="19aa5-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="19aa5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19aa5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19aa5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19aa5-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="19aa5-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="19aa5-121">Namespace</span></span><br/>                | <span data-ttu-id="19aa5-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="19aa5-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="19aa5-123">MOF</span><span class="sxs-lookup"><span data-stu-id="19aa5-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19aa5-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19aa5-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="19aa5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="19aa5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19aa5-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19aa5-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="19aa5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19aa5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19aa5-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="19aa5-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





