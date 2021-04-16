---
title: Die Methode "ltactiveserver" der Win32_RDMSEnvironment-Klasse
description: Legt den FQDN der RDMs-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Klasse "Win32_RDMSEnvironment"
- Win32_RDMSEnvironment Klasse Remotedesktopdienste, Methode "Methode"
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476419"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="aa70e-106">Die Methode "ltactiveserver" der Win32- \_ Klasse "rdmsenvironment"</span><span class="sxs-lookup"><span data-stu-id="aa70e-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="aa70e-107">Legt den FQDN der RDMs-Umgebung (Remotedesktop Management Services) auf den aktuellen Knoten fest.</span><span class="sxs-lookup"><span data-stu-id="aa70e-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa70e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa70e-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="aa70e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa70e-109">Parameters</span></span>

<span data-ttu-id="aa70e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa70e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa70e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa70e-111">Return value</span></span>

<span data-ttu-id="aa70e-112">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa70e-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa70e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa70e-113">Requirements</span></span>



| <span data-ttu-id="aa70e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa70e-114">Requirement</span></span> | <span data-ttu-id="aa70e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aa70e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa70e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa70e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa70e-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa70e-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="aa70e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa70e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa70e-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa70e-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="aa70e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa70e-120">Namespace</span></span><br/>                | <span data-ttu-id="aa70e-121">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="aa70e-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="aa70e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="aa70e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa70e-123"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa70e-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa70e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aa70e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa70e-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa70e-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="aa70e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa70e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa70e-127">**Win32- \_ rdmsenvironment**</span><span class="sxs-lookup"><span data-stu-id="aa70e-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





