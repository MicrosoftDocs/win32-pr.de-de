---
description: 'StopService-Methode der Msvm_CollectionManagementService-Klasse: Beendet den Dienst.'
ms.assetid: 26d0aa9f-f5ca-481f-9bed-6788b0dc2803
title: StopService-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f46b7416a3f17788cbfc0af5aacba014d680dbf6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119248"
---
# <a name="stopservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="568fc-103">StopService-Methode der Msvm \_ CollectionManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="568fc-103">StopService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="568fc-104">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="568fc-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="568fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="568fc-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="568fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="568fc-106">Parameters</span></span>

<span data-ttu-id="568fc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="568fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="568fc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="568fc-108">Return value</span></span>

<span data-ttu-id="568fc-109">Gibt bei Erfolg 0 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="568fc-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="568fc-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="568fc-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="568fc-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="568fc-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="568fc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="568fc-112">Requirements</span></span>



| <span data-ttu-id="568fc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="568fc-113">Requirement</span></span> | <span data-ttu-id="568fc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="568fc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="568fc-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="568fc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="568fc-116">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="568fc-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="568fc-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="568fc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="568fc-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="568fc-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="568fc-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="568fc-119">Namespace</span></span><br/>                | <span data-ttu-id="568fc-120">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="568fc-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="568fc-121">MOF</span><span class="sxs-lookup"><span data-stu-id="568fc-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="568fc-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="568fc-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="568fc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="568fc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="568fc-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="568fc-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="568fc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="568fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="568fc-126">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="568fc-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




