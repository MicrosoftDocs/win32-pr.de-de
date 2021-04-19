---
description: Fordert an, dass das Gerät seine Konfigurations-, Setup-und/oder Zustandsinformationen aus einem Sicherungs Speicher erneut einrichtet.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Restoreproperties-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362897"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="7e4e7-103">Restoreproperties-Methode der CIM \_ LogicalDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e4e7-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="7e4e7-104">Fordert an, dass das Gerät seine Konfigurations-, Setup-und/oder Zustandsinformationen aus einem Sicherungs Speicher erneut einrichtet.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="7e4e7-105">Die Absicht besteht darin, diese Informationen zu einem früheren Zeitpunkt (über die SaveProperties-Methode) zu erfassen und damit ein Gerät an diese frühere "Bedingung" zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="7e4e7-106">Diese Methode wird möglicherweise nicht von allen Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="7e4e7-107">Die Methode sollte bei erfolgreicher Ausführung 0 (null) zurückgeben, 1, wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="7e4e7-108">In einer Unterklasse können die möglichen Rückgabecodes mit einem ValueMap-Qualifizierer für die Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="7e4e7-109">Die Zeichen folgen, in die der ValueMap-Inhalt übersetzt wird, können auch in der Unterklasse als Werte Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e4e7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e4e7-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="7e4e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e4e7-111">Parameters</span></span>

<span data-ttu-id="7e4e7-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7e4e7-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e4e7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e4e7-113">Requirements</span></span>



| <span data-ttu-id="7e4e7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e4e7-114">Requirement</span></span> | <span data-ttu-id="7e4e7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e4e7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e4e7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e4e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e4e7-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7e4e7-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7e4e7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e4e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e4e7-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7e4e7-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7e4e7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e4e7-120">Namespace</span></span><br/>                | <span data-ttu-id="7e4e7-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e4e7-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e4e7-122">MOF</span><span class="sxs-lookup"><span data-stu-id="7e4e7-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e4e7-123"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e4e7-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e4e7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7e4e7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e4e7-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e4e7-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e4e7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e4e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e4e7-127">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7e4e7-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




