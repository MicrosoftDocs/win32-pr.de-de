---
title: Removedesktopzuweisung-Methode der Win32_RDMSDesktopAssignment-Klasse
description: Entfernt eine Desktop Zuweisung.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Removedesktopzuweisung-Methode Remotedesktopdienste
- Removedesktopzuweisung-Methode Remotedesktopdienste, Win32_RDMSDesktopAssignment-Klasse
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste, removedesktopzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344503"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="857ae-106">Removedesktopzuweisung-Methode der Win32- \_ Klasse rdmsdesktopzuweisung</span><span class="sxs-lookup"><span data-stu-id="857ae-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="857ae-107">Entfernt eine Desktop Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="857ae-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="857ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="857ae-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="857ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="857ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="857ae-110">*Collectionalias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="857ae-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857ae-111">Der sammlungsalias.</span><span class="sxs-lookup"><span data-stu-id="857ae-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="857ae-112">*Desktopname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="857ae-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857ae-113">Der Name des Desktops.</span><span class="sxs-lookup"><span data-stu-id="857ae-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="857ae-114">*Benutzer Domäne* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="857ae-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857ae-115">Der Domänen Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="857ae-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="857ae-116">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="857ae-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857ae-117">Der Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="857ae-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="857ae-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="857ae-118">Requirements</span></span>



| <span data-ttu-id="857ae-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="857ae-119">Requirement</span></span> | <span data-ttu-id="857ae-120">Wert</span><span class="sxs-lookup"><span data-stu-id="857ae-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="857ae-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="857ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="857ae-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="857ae-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="857ae-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="857ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="857ae-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="857ae-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="857ae-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="857ae-125">Namespace</span></span><br/>                | <span data-ttu-id="857ae-126">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="857ae-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="857ae-127">MOF</span><span class="sxs-lookup"><span data-stu-id="857ae-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857ae-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="857ae-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="857ae-129">DLL</span><span class="sxs-lookup"><span data-stu-id="857ae-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857ae-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857ae-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="857ae-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="857ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857ae-132">**Win32- \_ rdmsdesktopzuweisung**</span><span class="sxs-lookup"><span data-stu-id="857ae-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





