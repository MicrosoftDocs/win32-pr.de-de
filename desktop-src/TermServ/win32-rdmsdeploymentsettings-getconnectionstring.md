---
title: GetConnectionString-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- GetConnectionString-Methode Remotedesktopdienste
- GetConnectionString-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetConnectionString-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477082"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="26886-106">GetConnectionString-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="26886-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="26886-107">Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="26886-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="26886-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="26886-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="26886-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="26886-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26886-110">*ConnectionString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26886-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26886-111">Die Verbindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26886-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26886-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26886-112">Return value</span></span>

<span data-ttu-id="26886-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26886-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26886-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26886-114">Requirements</span></span>



| <span data-ttu-id="26886-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26886-115">Requirement</span></span> | <span data-ttu-id="26886-116">Wert</span><span class="sxs-lookup"><span data-stu-id="26886-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26886-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26886-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26886-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26886-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="26886-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26886-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26886-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="26886-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="26886-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="26886-121">Namespace</span></span><br/>                | <span data-ttu-id="26886-122">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="26886-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="26886-123">MOF</span><span class="sxs-lookup"><span data-stu-id="26886-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26886-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26886-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="26886-125">DLL</span><span class="sxs-lookup"><span data-stu-id="26886-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26886-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26886-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="26886-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26886-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26886-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="26886-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





