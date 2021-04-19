---
title: Getvirtualdesktopassignetdtouser-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Getvirtualdesktopassignetdtouser-Methode Remotedesktopdienste
- Getvirtualdesktopassignetdtouser-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getvirtualdesktopassignetdtouser-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339540"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="b6faf-106">Getvirtualdesktopassignetdtouser-Methode der Win32 \_ rdmsvirtualdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6faf-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="b6faf-107">Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b6faf-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6faf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6faf-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="b6faf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6faf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6faf-110">*Collectionalias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6faf-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6faf-111">Der Alias der Sammlung virtueller Desktops, die den virtuellen Desktop enthält.</span><span class="sxs-lookup"><span data-stu-id="b6faf-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="b6faf-112">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6faf-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6faf-113">Der Benutzername des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b6faf-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b6faf-114">*Benutzer Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6faf-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6faf-115">Der Domänen Name des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b6faf-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b6faf-116">*VMName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b6faf-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6faf-117">Empfängt den Namen des virtuellen Computers des virtuellen Desktops.</span><span class="sxs-lookup"><span data-stu-id="b6faf-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6faf-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6faf-118">Return value</span></span>

<span data-ttu-id="b6faf-119">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6faf-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6faf-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6faf-120">Requirements</span></span>



| <span data-ttu-id="b6faf-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6faf-121">Requirement</span></span> | <span data-ttu-id="b6faf-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b6faf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6faf-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6faf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b6faf-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6faf-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b6faf-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6faf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b6faf-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6faf-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b6faf-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6faf-127">Namespace</span></span><br/>                | <span data-ttu-id="b6faf-128">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="b6faf-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b6faf-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b6faf-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6faf-130"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b6faf-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6faf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b6faf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6faf-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6faf-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b6faf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6faf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6faf-134">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="b6faf-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





