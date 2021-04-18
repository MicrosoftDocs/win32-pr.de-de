---
title: Getclientaccessname-Methode der Win32_RDMSEnvironment-Klasse
description: Ruft den Namen der Domain Name System (DNS) Resource Record (RR) der Remotedesktop Management Services (RDMs)-Umgebung ab.
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Getclientaccessname-Methode Remotedesktopdienste
- Getclientaccessname-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, getclientaccessname-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337294"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="a23cf-106">Getclientaccessname-Methode der Win32 \_ rdmsenvironment-Klasse</span><span class="sxs-lookup"><span data-stu-id="a23cf-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="a23cf-107">Ruft den Namen der Domain Name System (DNS) Resource Record (RR) der Remotedesktop Management Services (RDMs)-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="a23cf-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a23cf-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="a23cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a23cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a23cf-110">*Clientaccessname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a23cf-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a23cf-111">Empfängt den abgerufenen RR-Namen.</span><span class="sxs-lookup"><span data-stu-id="a23cf-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a23cf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a23cf-112">Return value</span></span>

<span data-ttu-id="a23cf-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a23cf-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a23cf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a23cf-114">Requirements</span></span>



| <span data-ttu-id="a23cf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a23cf-115">Requirement</span></span> | <span data-ttu-id="a23cf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a23cf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a23cf-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a23cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a23cf-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a23cf-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a23cf-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a23cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a23cf-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a23cf-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a23cf-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a23cf-121">Namespace</span></span><br/>                | <span data-ttu-id="a23cf-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="a23cf-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a23cf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a23cf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a23cf-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a23cf-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a23cf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a23cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a23cf-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a23cf-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a23cf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a23cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23cf-128">**Win32- \_ rdmsenvironment**</span><span class="sxs-lookup"><span data-stu-id="a23cf-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





