---
description: Fordert an, dass das Gerät seine aktuellen Konfigurations-, Setup-und/oder Zustandsinformationen in einem Sicherungs Speicher erfasst.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: SaveProperties-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373305"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="05c21-103">SaveProperties-Methode der CIM \_ LogicalDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="05c21-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="05c21-104">Fordert an, dass das Gerät seine aktuellen Konfigurations-, Setup-und/oder Zustandsinformationen in einem Sicherungs Speicher erfasst.</span><span class="sxs-lookup"><span data-stu-id="05c21-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="05c21-105">Das Ziel besteht darin, diese Informationen zu einem späteren Zeitpunkt (über die restoreproperties-Methode) zu verwenden, um ein Gerät an seine vorhandene "Bedingung" zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="05c21-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="05c21-106">Diese Methode wird möglicherweise nicht von allen Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05c21-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="05c21-107">Die Methode sollte bei erfolgreicher Ausführung 0 (null) zurückgeben, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="05c21-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="05c21-108">In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05c21-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="05c21-109">Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05c21-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c21-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="05c21-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="05c21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="05c21-111">Parameters</span></span>

<span data-ttu-id="05c21-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="05c21-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05c21-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05c21-113">Return value</span></span>

<span data-ttu-id="05c21-114">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05c21-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c21-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05c21-115">Requirements</span></span>



| <span data-ttu-id="05c21-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05c21-116">Requirement</span></span> | <span data-ttu-id="05c21-117">Wert</span><span class="sxs-lookup"><span data-stu-id="05c21-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c21-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05c21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05c21-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05c21-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="05c21-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05c21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05c21-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="05c21-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="05c21-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="05c21-122">Namespace</span></span><br/>                | <span data-ttu-id="05c21-123">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="05c21-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05c21-124">MOF</span><span class="sxs-lookup"><span data-stu-id="05c21-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05c21-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05c21-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05c21-126">DLL</span><span class="sxs-lookup"><span data-stu-id="05c21-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05c21-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05c21-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05c21-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05c21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c21-129">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="05c21-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




