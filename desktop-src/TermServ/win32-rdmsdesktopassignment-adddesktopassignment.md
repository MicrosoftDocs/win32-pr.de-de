---
title: Adddesktopzuweisung-Methode der Win32_RDMSDesktopAssignment-Klasse
description: Fügen Sie eine Desktop Zuweisung hinzu.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Adddesktopzuweisung-Methode Remotedesktopdienste
- Adddesktopzuweisung-Methode Remotedesktopdienste, Win32_RDMSDesktopAssignment-Klasse
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste, adddesktopzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858807"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="43bff-106">Adddesktopzuweisung-Methode der Win32- \_ Klasse rdmsdesktopzuweisung</span><span class="sxs-lookup"><span data-stu-id="43bff-106">AddDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="43bff-107">Hinzufügen einer Desktop Zuweisung</span><span class="sxs-lookup"><span data-stu-id="43bff-107">Add a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="43bff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="43bff-108">Syntax</span></span>


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="43bff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43bff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43bff-110">*Collectionalias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43bff-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43bff-111">Der sammlungsalias.</span><span class="sxs-lookup"><span data-stu-id="43bff-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="43bff-112">*Desktopname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43bff-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43bff-113">Der Name des Desktops.</span><span class="sxs-lookup"><span data-stu-id="43bff-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="43bff-114">*Benutzer Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43bff-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43bff-115">Der Domänen Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="43bff-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="43bff-116">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43bff-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43bff-117">Der Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="43bff-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43bff-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43bff-118">Requirements</span></span>



| <span data-ttu-id="43bff-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43bff-119">Requirement</span></span> | <span data-ttu-id="43bff-120">Wert</span><span class="sxs-lookup"><span data-stu-id="43bff-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bff-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43bff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43bff-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="43bff-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="43bff-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43bff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43bff-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="43bff-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="43bff-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="43bff-125">Namespace</span></span><br/>                | <span data-ttu-id="43bff-126">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="43bff-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="43bff-127">MOF</span><span class="sxs-lookup"><span data-stu-id="43bff-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43bff-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="43bff-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="43bff-129">DLL</span><span class="sxs-lookup"><span data-stu-id="43bff-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43bff-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43bff-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="43bff-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43bff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43bff-132">**Win32- \_ rdmsdesktopzuweisung**</span><span class="sxs-lookup"><span data-stu-id="43bff-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





