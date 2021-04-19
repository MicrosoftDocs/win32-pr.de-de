---
title: SetInt32Property-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346333"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="4fd5e-106">SetInt32Property-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fd5e-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="4fd5e-107">Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="4fd5e-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd5e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fd5e-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="4fd5e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fd5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd5e-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd5e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd5e-111">Der Alias für die Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="4fd5e-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="4fd5e-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd5e-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd5e-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="4fd5e-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fd5e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fd5e-114">Requirements</span></span>



| <span data-ttu-id="4fd5e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fd5e-115">Requirement</span></span> | <span data-ttu-id="4fd5e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4fd5e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd5e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fd5e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd5e-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4fd5e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4fd5e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fd5e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd5e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4fd5e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4fd5e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fd5e-121">Namespace</span></span><br/>                | <span data-ttu-id="4fd5e-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="4fd5e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4fd5e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4fd5e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fd5e-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fd5e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fd5e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4fd5e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fd5e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd5e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4fd5e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fd5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd5e-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="4fd5e-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





