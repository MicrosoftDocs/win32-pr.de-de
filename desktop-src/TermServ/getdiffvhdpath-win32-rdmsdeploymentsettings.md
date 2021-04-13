---
title: Getdiffvhdpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den Verzeichnispfad ab, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Getdiffvhdpath-Methode Remotedesktopdienste
- Getdiffvhdpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getdiffvhdpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391610"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5ff57-106">Getdiffvhdpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ff57-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5ff57-107">Ruft den Verzeichnispfad ab, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5ff57-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff57-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ff57-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="5ff57-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ff57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff57-110">*Directoriypath* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ff57-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff57-111">Empfängt den neuen differenzierenden Datenträger Pfad.</span><span class="sxs-lookup"><span data-stu-id="5ff57-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff57-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ff57-112">Return value</span></span>

<span data-ttu-id="5ff57-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ff57-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff57-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ff57-114">Requirements</span></span>



| <span data-ttu-id="5ff57-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ff57-115">Requirement</span></span> | <span data-ttu-id="5ff57-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5ff57-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff57-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ff57-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff57-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ff57-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ff57-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ff57-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff57-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ff57-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ff57-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ff57-121">Namespace</span></span><br/>                | <span data-ttu-id="5ff57-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="5ff57-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ff57-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5ff57-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ff57-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ff57-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ff57-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5ff57-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ff57-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ff57-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ff57-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ff57-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff57-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="5ff57-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





