---
description: Der Dienst wird in den Zustand "beendet" versetzt.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Stop Service-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862863"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="88daf-103">Stop Service-Methode der CIM_Service-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="88daf-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="88daf-104">Der Dienst wird in den Zustand "beendet" versetzt.</span><span class="sxs-lookup"><span data-stu-id="88daf-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="88daf-105">Die Semantik dieser Methode überschneidet sich mit der **requestStateChange** -Methode, die von [**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="88daf-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="88daf-106">Diese Methode wird beibehalten, da Sie weitgehend implementiert wurde und ihre einfache "Ende"-Semantik praktisch verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="88daf-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="88daf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88daf-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="88daf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88daf-108">Parameters</span></span>

<span data-ttu-id="88daf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="88daf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88daf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88daf-110">Return value</span></span>

<span data-ttu-id="88daf-111">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88daf-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="88daf-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88daf-112">Requirements</span></span>



| <span data-ttu-id="88daf-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88daf-113">Requirement</span></span> | <span data-ttu-id="88daf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="88daf-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88daf-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88daf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="88daf-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="88daf-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="88daf-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88daf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="88daf-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="88daf-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="88daf-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="88daf-119">Namespace</span></span><br/>                | <span data-ttu-id="88daf-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="88daf-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88daf-121">MOF</span><span class="sxs-lookup"><span data-stu-id="88daf-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88daf-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="88daf-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88daf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="88daf-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88daf-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88daf-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88daf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88daf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88daf-126">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="88daf-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




