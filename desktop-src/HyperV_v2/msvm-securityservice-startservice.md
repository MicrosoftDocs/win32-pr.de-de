---
description: 'StartService-Methode der Msvm_SecurityService-Klasse: Startet den Dienst.'
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: StartService-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111398"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="e2715-103">StartService-Methode der Msvm \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2715-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="e2715-104">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="e2715-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2715-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2715-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e2715-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2715-106">Parameters</span></span>

<span data-ttu-id="e2715-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e2715-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2715-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2715-108">Return value</span></span>

<span data-ttu-id="e2715-109">Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2715-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e2715-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e2715-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2715-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e2715-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2715-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2715-112">Requirements</span></span>



| <span data-ttu-id="e2715-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2715-113">Requirement</span></span> | <span data-ttu-id="e2715-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e2715-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2715-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2715-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e2715-116">Windows 10, nur Desktop-Apps der Version 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2715-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e2715-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2715-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e2715-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e2715-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e2715-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2715-119">Namespace</span></span><br/>                | <span data-ttu-id="e2715-120">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2715-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e2715-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e2715-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2715-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2715-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2715-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e2715-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2715-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2715-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2715-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2715-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2715-126">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="e2715-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




