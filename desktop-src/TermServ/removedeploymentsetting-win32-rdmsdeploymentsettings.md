---
title: Removedeploymentsetting-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Löscht die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Removedeploymentsetting-Methode Remotedesktopdienste
- Removedeploymentsetting-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, removedeploymentsetting-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859261"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="2fc4f-106">Removedeploymentsetting-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="2fc4f-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="2fc4f-107">Löscht die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc4f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc4f-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="2fc4f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc4f-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fc4f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc4f-111">Der Alias der Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fc4f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fc4f-112">Requirements</span></span>



| <span data-ttu-id="2fc4f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fc4f-113">Requirement</span></span> | <span data-ttu-id="2fc4f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2fc4f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc4f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fc4f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc4f-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2fc4f-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2fc4f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fc4f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc4f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fc4f-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2fc4f-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fc4f-119">Namespace</span></span><br/>                | <span data-ttu-id="2fc4f-120">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="2fc4f-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2fc4f-121">MOF</span><span class="sxs-lookup"><span data-stu-id="2fc4f-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fc4f-122"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2fc4f-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fc4f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc4f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fc4f-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fc4f-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2fc4f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fc4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc4f-126">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="2fc4f-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





