---
title: Getactiveserver-Methode der Win32_RDMSEnvironment-Klasse
description: Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung (Remotedesktop Management Services) ab.
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Getactiveserver-Methode Remotedesktopdienste
- Getactiveserver-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, getactiveserver-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477457"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="e51fd-106">Getactiveserver-Methode der Win32 \_ rdmsenvironment-Klasse</span><span class="sxs-lookup"><span data-stu-id="e51fd-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="e51fd-107">Ruft den voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN) der RDMs-Umgebung (Remotedesktop Management Services) ab.</span><span class="sxs-lookup"><span data-stu-id="e51fd-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e51fd-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="e51fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e51fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51fd-110">*Servername* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e51fd-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e51fd-111">Empfängt den abgerufenen FQDN.</span><span class="sxs-lookup"><span data-stu-id="e51fd-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51fd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e51fd-112">Return value</span></span>

<span data-ttu-id="e51fd-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e51fd-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e51fd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e51fd-114">Requirements</span></span>



| <span data-ttu-id="e51fd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e51fd-115">Requirement</span></span> | <span data-ttu-id="e51fd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e51fd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e51fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e51fd-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e51fd-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e51fd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e51fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e51fd-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e51fd-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e51fd-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e51fd-121">Namespace</span></span><br/>                | <span data-ttu-id="e51fd-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="e51fd-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e51fd-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e51fd-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e51fd-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e51fd-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e51fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e51fd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e51fd-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e51fd-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e51fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e51fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51fd-128">**Win32- \_ rdmsenvironment**</span><span class="sxs-lookup"><span data-stu-id="e51fd-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





