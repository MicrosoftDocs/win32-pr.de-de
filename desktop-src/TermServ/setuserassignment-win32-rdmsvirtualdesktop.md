---
title: Setuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Weist einem Benutzer einen virtuellen Desktop zu.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Setuserzuweisung-Methode Remotedesktopdienste
- Setuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, setuserzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345926"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="cb2f2-106">Setuserzuweisungs-Methode der Win32 \_ -Klasse rdmsvirtualdesktop</span><span class="sxs-lookup"><span data-stu-id="cb2f2-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="cb2f2-107">Weist einem Benutzer einen virtuellen Desktop zu.</span><span class="sxs-lookup"><span data-stu-id="cb2f2-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb2f2-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="cb2f2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb2f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb2f2-110">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb2f2-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb2f2-111">Der Benutzername des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cb2f2-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="cb2f2-112">*Benutzer Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb2f2-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb2f2-113">Der Domänen Name des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cb2f2-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb2f2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb2f2-114">Return value</span></span>

<span data-ttu-id="cb2f2-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb2f2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2f2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb2f2-116">Requirements</span></span>



| <span data-ttu-id="cb2f2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb2f2-117">Requirement</span></span> | <span data-ttu-id="cb2f2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cb2f2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2f2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb2f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2f2-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb2f2-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cb2f2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb2f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2f2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb2f2-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cb2f2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb2f2-123">Namespace</span></span><br/>                | <span data-ttu-id="cb2f2-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="cb2f2-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cb2f2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="cb2f2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb2f2-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cb2f2-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb2f2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cb2f2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb2f2-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb2f2-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cb2f2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb2f2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2f2-130">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="cb2f2-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





