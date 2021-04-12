---
description: Fordert eine zurück setzung des LogicalDevice an.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Reset-Methode der CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347798"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="26694-103">Reset-Methode der CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="26694-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="26694-104">Fordert eine zurück setzung des LogicalDevice an.</span><span class="sxs-lookup"><span data-stu-id="26694-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="26694-105">In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26694-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="26694-106">Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26694-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="26694-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26694-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="26694-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26694-108">Parameters</span></span>

<span data-ttu-id="26694-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="26694-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26694-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26694-110">Return value</span></span>

<span data-ttu-id="26694-111">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26694-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="26694-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26694-112">Requirements</span></span>



| <span data-ttu-id="26694-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26694-113">Requirement</span></span> | <span data-ttu-id="26694-114">Wert</span><span class="sxs-lookup"><span data-stu-id="26694-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26694-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26694-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26694-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="26694-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="26694-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26694-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26694-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="26694-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="26694-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="26694-119">Namespace</span></span><br/>                | <span data-ttu-id="26694-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="26694-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26694-121">MOF</span><span class="sxs-lookup"><span data-stu-id="26694-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26694-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26694-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26694-123">DLL</span><span class="sxs-lookup"><span data-stu-id="26694-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26694-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26694-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26694-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26694-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26694-126">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="26694-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




