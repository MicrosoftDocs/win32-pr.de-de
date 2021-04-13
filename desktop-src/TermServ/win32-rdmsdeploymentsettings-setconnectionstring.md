---
title: SetConnectionString-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Legt die Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- SetConnectionString-Methode Remotedesktopdienste
- SetConnectionString-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setConnectionString-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391806"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="3da5b-106">SetConnectionString-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="3da5b-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="3da5b-107">Legt die Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.</span><span class="sxs-lookup"><span data-stu-id="3da5b-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da5b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3da5b-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="3da5b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3da5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da5b-110">*ConnectionString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3da5b-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3da5b-111">Die festzulegende Verbindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3da5b-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da5b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3da5b-112">Return value</span></span>

<span data-ttu-id="3da5b-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3da5b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da5b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da5b-114">Requirements</span></span>



| <span data-ttu-id="3da5b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3da5b-115">Requirement</span></span> | <span data-ttu-id="3da5b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3da5b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da5b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3da5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3da5b-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3da5b-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3da5b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3da5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3da5b-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3da5b-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="3da5b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3da5b-121">Namespace</span></span><br/>                | <span data-ttu-id="3da5b-122">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="3da5b-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3da5b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3da5b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3da5b-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3da5b-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3da5b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3da5b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3da5b-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da5b-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3da5b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3da5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da5b-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="3da5b-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





