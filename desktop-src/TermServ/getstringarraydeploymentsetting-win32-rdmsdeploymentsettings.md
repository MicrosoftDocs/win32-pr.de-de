---
title: Getstringarraydeploymentsetting-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops ab.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Getstringarraydeploymentsetting-Methode Remotedesktopdienste
- Getstringarraydeploymentsetting-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getstringarraydeploymentsetting-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103170"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="6e3e1-106">Getstringarraydeploymentsetting-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e3e1-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="6e3e1-107">Ruft die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="6e3e1-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e3e1-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="6e3e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e3e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e3e1-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3e1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3e1-111">Der Alias der Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="6e3e1-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="6e3e1-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6e3e1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3e1-113">Empfängt ein Array von Zeichen folgen, das die Bereitstellungs Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="6e3e1-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e3e1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e3e1-114">Requirements</span></span>



| <span data-ttu-id="6e3e1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e3e1-115">Requirement</span></span> | <span data-ttu-id="6e3e1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6e3e1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3e1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e3e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3e1-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e3e1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6e3e1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e3e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3e1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e3e1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6e3e1-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e3e1-121">Namespace</span></span><br/>                | <span data-ttu-id="6e3e1-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="6e3e1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6e3e1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6e3e1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e3e1-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e3e1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e3e1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e3e1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e3e1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e3e1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6e3e1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e3e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3e1-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="6e3e1-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





