---
description: Die onlinedevice-Methode wurde als veraltet markiert, anstelle der allgemeineren requestStateChange-Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Onlinedevice-Methode der CIM_LogicalDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351041"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="7af32-103">Onlinedevice-Methode der CIM \_ LogicalDevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7af32-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="7af32-104">Die **onlinedevice** -Methode wurde als veraltet markiert, anstelle der allgemeineren **requestStateChange** -Methode, die sich direkt mit der von dieser Methode bereitgestellten Funktionalität überlappt.</span><span class="sxs-lookup"><span data-stu-id="7af32-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af32-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="7af32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7af32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af32-107">*Online* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7af32-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af32-108">Wenn der Wert **true** ist, schalten Sie das Gerät online, und schalten Sie das Gerät bei **false** offline.</span><span class="sxs-lookup"><span data-stu-id="7af32-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af32-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7af32-109">Return value</span></span>

<span data-ttu-id="7af32-110">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7af32-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af32-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7af32-111">Requirements</span></span>



| <span data-ttu-id="7af32-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7af32-112">Requirement</span></span> | <span data-ttu-id="7af32-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7af32-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af32-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7af32-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7af32-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7af32-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7af32-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7af32-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7af32-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7af32-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7af32-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7af32-118">Namespace</span></span><br/>                | <span data-ttu-id="7af32-119">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7af32-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7af32-120">MOF</span><span class="sxs-lookup"><span data-stu-id="7af32-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7af32-121"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7af32-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7af32-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7af32-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7af32-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7af32-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7af32-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7af32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af32-125">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="7af32-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




