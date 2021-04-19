---
title: Removeuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Entfernt die Benutzer Zuweisung vom virtuellen Desktop.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Removeuserzuweisungs-Methode Remotedesktopdienste
- Removeuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, removeuserzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345903"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="6a079-106">Removeuserzuweisungs-Methode der Win32 \_ rdmsvirtualdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="6a079-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="6a079-107">Entfernt die Benutzer Zuweisung vom virtuellen Desktop.</span><span class="sxs-lookup"><span data-stu-id="6a079-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a079-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a079-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="6a079-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a079-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a079-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a079-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a079-111">Der Name des virtuellen Computers des virtuellen Desktops.</span><span class="sxs-lookup"><span data-stu-id="6a079-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a079-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a079-112">Return value</span></span>

<span data-ttu-id="6a079-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a079-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a079-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a079-114">Requirements</span></span>



| <span data-ttu-id="6a079-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a079-115">Requirement</span></span> | <span data-ttu-id="6a079-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6a079-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a079-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a079-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a079-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a079-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6a079-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a079-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a079-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a079-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6a079-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a079-121">Namespace</span></span><br/>                | <span data-ttu-id="6a079-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="6a079-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6a079-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6a079-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a079-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6a079-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a079-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a079-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a079-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a079-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6a079-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a079-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a079-128">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="6a079-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





