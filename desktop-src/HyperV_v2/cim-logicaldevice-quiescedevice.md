---
description: Die Methode "quiescedevice" wurde als veraltet markiert, anstelle der allgemeineren Methode "requestStateChange", die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Quiescedevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347808"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="b200e-103">Quiescedevice-Methode der CIM \_ LogicalDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b200e-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="b200e-104">Die Methode " **quiescedevice** " wurde als veraltet markiert, anstelle der allgemeineren Methode " **requestStateChange** ", die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.</span><span class="sxs-lookup"><span data-stu-id="b200e-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b200e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b200e-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="b200e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b200e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b200e-107">Inaktiven Status  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b200e-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b200e-108">Bei Festlegung auf **true** beenden Sie alle Aktivitäten ordnungsgemäß, wenn die Aktivität **false** fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="b200e-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b200e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b200e-109">Return value</span></span>

<span data-ttu-id="b200e-110">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b200e-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b200e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b200e-111">Requirements</span></span>



| <span data-ttu-id="b200e-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b200e-112">Requirement</span></span> | <span data-ttu-id="b200e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b200e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b200e-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b200e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b200e-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b200e-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b200e-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b200e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b200e-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b200e-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b200e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b200e-118">Namespace</span></span><br/>                | <span data-ttu-id="b200e-119">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b200e-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b200e-120">MOF</span><span class="sxs-lookup"><span data-stu-id="b200e-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b200e-121"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b200e-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b200e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b200e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b200e-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b200e-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b200e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b200e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b200e-125">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b200e-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




