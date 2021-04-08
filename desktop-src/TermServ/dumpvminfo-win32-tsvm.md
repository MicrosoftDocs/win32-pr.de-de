---
title: Dumpvminfo-Methode der Win32_TSVm-Klasse
description: Dieser Member dient zu internen Testzwecken und sollte nicht in Ihrem Code verwendet werden.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Dumpvminfo-Methode Remotedesktopdienste
- Dumpvminfo-Methode Remotedesktopdienste, Win32_TSVm-Klasse
- Win32_TSVm-Klasse Remotedesktopdienste, dumpvminfo-Methode
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743848"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="6a54e-106">Dumpvminfo-Methode der Win32- \_ Klasse "ZVM"</span><span class="sxs-lookup"><span data-stu-id="6a54e-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="6a54e-107">Dieser Member dient zu internen Testzwecken und sollte nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a54e-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a54e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a54e-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="6a54e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a54e-109">Parameters</span></span>

<span data-ttu-id="6a54e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6a54e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a54e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a54e-111">Return value</span></span>

<span data-ttu-id="6a54e-112">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a54e-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6a54e-113">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6a54e-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a54e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a54e-114">Requirements</span></span>



| <span data-ttu-id="6a54e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a54e-115">Requirement</span></span> | <span data-ttu-id="6a54e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6a54e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a54e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a54e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a54e-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a54e-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="6a54e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a54e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a54e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a54e-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="6a54e-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a54e-121">Namespace</span></span><br/>                | <span data-ttu-id="6a54e-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6a54e-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="6a54e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6a54e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a54e-124"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="6a54e-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="6a54e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6a54e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a54e-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a54e-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a54e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a54e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a54e-128">**Win32- \_ VM**</span><span class="sxs-lookup"><span data-stu-id="6a54e-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





