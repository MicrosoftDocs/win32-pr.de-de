---
title: Addvirtualdesktop-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Fügt der Sammlung virtueller Desktops einen virtuellen Desktop hinzu.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Addvirtualdesktop-Methode Remotedesktopdienste
- Addvirtualdesktop-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, addvirtualdesktop-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517498"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="3bc79-106">Addvirtualdesktop-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="3bc79-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="3bc79-107">Fügt der Sammlung virtueller Desktops einen virtuellen Desktop hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bc79-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc79-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bc79-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="3bc79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bc79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc79-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bc79-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bc79-111">Der Name des virtuellen Computers, der den virtuellen Desktop hostet.</span><span class="sxs-lookup"><span data-stu-id="3bc79-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc79-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bc79-112">Return value</span></span>

<span data-ttu-id="3bc79-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3bc79-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc79-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bc79-114">Requirements</span></span>



| <span data-ttu-id="3bc79-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bc79-115">Requirement</span></span> | <span data-ttu-id="3bc79-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3bc79-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc79-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bc79-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc79-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3bc79-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3bc79-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bc79-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc79-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bc79-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3bc79-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bc79-121">Namespace</span></span><br/>                | <span data-ttu-id="3bc79-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="3bc79-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3bc79-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3bc79-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bc79-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3bc79-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bc79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bc79-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc79-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3bc79-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bc79-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc79-128">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="3bc79-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





