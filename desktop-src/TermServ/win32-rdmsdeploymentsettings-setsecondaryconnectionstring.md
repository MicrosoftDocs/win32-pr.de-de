---
title: Setsecondaryconnectionstring-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Legt die sekundäre Verbindungs Zeichenfolge für die Bereitstellungs Ebene fest.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- Setsecondaryconnectionstring-Methode Remotedesktopdienste
- Setsecondaryconnectionstring-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setsecondaryconnectionstring-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741104"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="60088-106">Setsecondaryconnectionstring-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="60088-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="60088-107">Legt die sekundäre Verbindungs Zeichenfolge für die Bereitstellungs Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="60088-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="60088-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60088-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="60088-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60088-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60088-110">*Secondaryconnectionstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60088-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60088-111">Die festzulegende Verbindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="60088-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60088-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60088-112">Return value</span></span>

<span data-ttu-id="60088-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60088-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60088-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60088-114">Requirements</span></span>



| <span data-ttu-id="60088-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60088-115">Requirement</span></span> | <span data-ttu-id="60088-116">Wert</span><span class="sxs-lookup"><span data-stu-id="60088-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60088-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60088-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60088-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="60088-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="60088-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60088-119">Minimum supported server</span></span><br/> | <span data-ttu-id="60088-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60088-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="60088-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="60088-121">Namespace</span></span><br/>                | <span data-ttu-id="60088-122">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="60088-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="60088-123">MOF</span><span class="sxs-lookup"><span data-stu-id="60088-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60088-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60088-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="60088-125">DLL</span><span class="sxs-lookup"><span data-stu-id="60088-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60088-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60088-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="60088-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60088-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60088-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="60088-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





