---
description: Die enableDevice-Methode wurde anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt, als veraltet markiert.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: EnableDevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362576"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="c811d-103">EnableDevice-Methode der CIM \_ LogicalDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c811d-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="c811d-104">Die enableDevice-Methode wurde anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt, als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="c811d-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="c811d-105">Fordert an, dass das LogicalDevice aktiviert ("aktivierter" Eingabeparameter = true) oder deaktiviert (= false) ist.</span><span class="sxs-lookup"><span data-stu-id="c811d-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="c811d-106">Bei erfolgreicher Ausführung sollte die Status Eigenschaften des Geräts den gewünschten Zustand (aktiviert/deaktiviert) widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="c811d-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="c811d-107">Beachten Sie, dass sich die Funktion dieser Methode mit der Eigenschaft requestedstate überlappt.</span><span class="sxs-lookup"><span data-stu-id="c811d-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="c811d-108">Requestedstate wurde dem Modell hinzugefügt, um einen Datensatz (d. h. einen beibehaltenen Wert) der letzten Zustands Anforderung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="c811d-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="c811d-109">Beim Aufrufen der enableDevice-Methode sollte die requestedstate-Eigenschaft entsprechend festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c811d-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="c811d-110">Der Rückgabecode sollte 0 sein, wenn die Anforderung erfolgreich ausgeführt wurde. der Rückgabecode ist 1, wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c811d-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="c811d-111">In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c811d-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="c811d-112">Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c811d-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="c811d-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="c811d-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="c811d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c811d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c811d-115">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c811d-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c811d-116">Wenn true, wird das Gerät aktiviert, wenn das Gerät durch false deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c811d-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c811d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c811d-117">Return value</span></span>

<span data-ttu-id="c811d-118">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c811d-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c811d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c811d-119">Requirements</span></span>



| <span data-ttu-id="c811d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c811d-120">Requirement</span></span> | <span data-ttu-id="c811d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c811d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c811d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c811d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c811d-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c811d-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c811d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c811d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c811d-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c811d-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c811d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c811d-126">Namespace</span></span><br/>                | <span data-ttu-id="c811d-127">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c811d-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c811d-128">MOF</span><span class="sxs-lookup"><span data-stu-id="c811d-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c811d-129"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c811d-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c811d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c811d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c811d-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c811d-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c811d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c811d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c811d-133">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c811d-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




