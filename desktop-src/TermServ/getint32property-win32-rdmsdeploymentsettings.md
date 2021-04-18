---
title: GetInt32Property-Methode der Win32_RDMSDeploymentSettings-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344070"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="8e334-106">GetInt32Property-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e334-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="8e334-107">Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="8e334-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e334-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e334-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="8e334-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e334-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e334-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e334-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e334-111">Der Alias für die Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="8e334-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="8e334-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e334-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e334-113">Eine ganze Zahl, die den abgerufenen Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="8e334-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e334-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e334-114">Requirements</span></span>



| <span data-ttu-id="8e334-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e334-115">Requirement</span></span> | <span data-ttu-id="8e334-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8e334-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e334-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e334-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e334-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e334-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="8e334-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e334-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e334-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e334-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="8e334-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e334-121">Namespace</span></span><br/>                | <span data-ttu-id="8e334-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="8e334-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="8e334-123">Header</span><span class="sxs-lookup"><span data-stu-id="8e334-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e334-124"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e334-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="8e334-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8e334-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e334-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e334-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="8e334-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8e334-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e334-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e334-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="8e334-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e334-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e334-130">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="8e334-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





