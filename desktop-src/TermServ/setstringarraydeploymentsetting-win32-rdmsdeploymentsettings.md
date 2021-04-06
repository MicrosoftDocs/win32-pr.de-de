---
title: Setstringarraydeploymentsetting-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Setstringarraydeploymentsetting-Methode Remotedesktopdienste
- Setstringarraydeploymentsetting-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setstringarraydeploymentsetting-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743489"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="fcc96-106">Setstringarraydeploymentsetting-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="fcc96-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="fcc96-107">Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fcc96-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcc96-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="fcc96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcc96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc96-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcc96-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc96-111">Der Alias der Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="fcc96-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="fcc96-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcc96-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc96-113">Ein Array von Zeichen folgen, das die neuen Bereitstellungs Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="fcc96-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcc96-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcc96-114">Requirements</span></span>



| <span data-ttu-id="fcc96-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcc96-115">Requirement</span></span> | <span data-ttu-id="fcc96-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fcc96-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc96-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcc96-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc96-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fcc96-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fcc96-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcc96-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc96-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcc96-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fcc96-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcc96-121">Namespace</span></span><br/>                | <span data-ttu-id="fcc96-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="fcc96-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fcc96-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fcc96-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcc96-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fcc96-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcc96-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fcc96-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcc96-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcc96-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fcc96-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcc96-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc96-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="fcc96-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





