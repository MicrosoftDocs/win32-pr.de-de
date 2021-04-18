---
title: Setbasevhdpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden. | Setbasevhdpath-Methode der Win32_RDMSDeploymentSettings-Klasse
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Setbasevhdpath-Methode Remotedesktopdienste
- Setbasevhdpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setbasevhdpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354299"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="9af05-107">Setbasevhdpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="9af05-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="9af05-108">Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9af05-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af05-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9af05-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="9af05-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9af05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af05-111">*Directoriypath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9af05-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af05-112">Der neue VHD-Bereitstellungs Pfad.</span><span class="sxs-lookup"><span data-stu-id="9af05-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af05-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9af05-113">Return value</span></span>

<span data-ttu-id="9af05-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9af05-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9af05-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9af05-115">Requirements</span></span>



| <span data-ttu-id="9af05-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9af05-116">Requirement</span></span> | <span data-ttu-id="9af05-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9af05-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af05-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9af05-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9af05-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9af05-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9af05-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9af05-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9af05-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9af05-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9af05-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9af05-122">Namespace</span></span><br/>                | <span data-ttu-id="9af05-123">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="9af05-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9af05-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9af05-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af05-125"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9af05-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af05-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9af05-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af05-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af05-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9af05-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9af05-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af05-129">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="9af05-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





