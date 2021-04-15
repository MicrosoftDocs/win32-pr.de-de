---
title: Removevirtualdesktop-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Entfernt einen virtuellen Desktop aus der Sammlung virtueller Desktops.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Removevirtualdesktop-Methode Remotedesktopdienste
- Removevirtualdesktop-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, removevirtualdesktop-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517528"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="63847-106">Removevirtualdesktop-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="63847-106">RemoveVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="63847-107">Entfernt einen virtuellen Desktop aus der Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="63847-107">Removes a virtual desktop from the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="63847-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="63847-108">Syntax</span></span>


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="63847-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63847-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63847-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63847-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63847-111">Der Name des virtuellen Computers, der den virtuellen Desktop hostet.</span><span class="sxs-lookup"><span data-stu-id="63847-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63847-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63847-112">Return value</span></span>

<span data-ttu-id="63847-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63847-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63847-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63847-114">Requirements</span></span>



| <span data-ttu-id="63847-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63847-115">Requirement</span></span> | <span data-ttu-id="63847-116">Wert</span><span class="sxs-lookup"><span data-stu-id="63847-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="63847-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63847-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63847-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="63847-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="63847-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63847-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63847-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63847-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="63847-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="63847-121">Namespace</span></span><br/>                | <span data-ttu-id="63847-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="63847-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="63847-123">MOF</span><span class="sxs-lookup"><span data-stu-id="63847-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63847-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="63847-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="63847-125">DLL</span><span class="sxs-lookup"><span data-stu-id="63847-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63847-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63847-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="63847-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63847-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63847-128">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="63847-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





