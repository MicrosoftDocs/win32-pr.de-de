---
description: 'StopService-Methode der Msvm_SecurityService-Klasse: Beendet den Dienst.'
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: StopService-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a9a16fef951fdee5ed7fc580da61f43d848a8dec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118708"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="b71aa-103">StopService-Methode der Msvm \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="b71aa-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="b71aa-104">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b71aa-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b71aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b71aa-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="b71aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b71aa-106">Parameters</span></span>

<span data-ttu-id="b71aa-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b71aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b71aa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b71aa-108">Return value</span></span>

<span data-ttu-id="b71aa-109">Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b71aa-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b71aa-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b71aa-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b71aa-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b71aa-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b71aa-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b71aa-112">Requirements</span></span>



| <span data-ttu-id="b71aa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b71aa-113">Requirement</span></span> | <span data-ttu-id="b71aa-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b71aa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b71aa-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b71aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b71aa-116">Windows 10, nur Desktop-Apps der Version 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="b71aa-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b71aa-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b71aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b71aa-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b71aa-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b71aa-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="b71aa-119">Namespace</span></span><br/>                | <span data-ttu-id="b71aa-120">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b71aa-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b71aa-121">MOF</span><span class="sxs-lookup"><span data-stu-id="b71aa-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b71aa-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b71aa-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b71aa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b71aa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b71aa-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b71aa-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b71aa-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b71aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71aa-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="b71aa-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




