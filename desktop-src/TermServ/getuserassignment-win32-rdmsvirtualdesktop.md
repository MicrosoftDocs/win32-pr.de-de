---
title: Getuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Getuserzuweisungs-Methode Remotedesktopdienste
- Getuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getuserzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392033"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="2efdd-106">Getuserzuweisungs-Methode der Win32 \_ rdmsvirtualdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="2efdd-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="2efdd-107">Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="2efdd-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="2efdd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2efdd-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="2efdd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2efdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2efdd-110">*Benutzername* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2efdd-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2efdd-111">Empfängt den Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="2efdd-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="2efdd-112">*Benutzer Domäne* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2efdd-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2efdd-113">Empfängt den Domänen Namen.</span><span class="sxs-lookup"><span data-stu-id="2efdd-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2efdd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2efdd-114">Return value</span></span>

<span data-ttu-id="2efdd-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2efdd-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2efdd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2efdd-116">Requirements</span></span>



| <span data-ttu-id="2efdd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efdd-117">Requirement</span></span> | <span data-ttu-id="2efdd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2efdd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2efdd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2efdd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2efdd-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2efdd-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2efdd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2efdd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2efdd-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2efdd-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2efdd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2efdd-123">Namespace</span></span><br/>                | <span data-ttu-id="2efdd-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="2efdd-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2efdd-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2efdd-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2efdd-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2efdd-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2efdd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2efdd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2efdd-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2efdd-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2efdd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2efdd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efdd-130">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="2efdd-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





