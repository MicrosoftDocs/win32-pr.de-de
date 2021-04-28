---
description: 'StopService-Methode der Msvm_TerminalService-Klasse: Beendet den Dienst.'
ms.assetid: c96ca784-c935-41a4-b1aa-8360cf270c9e
title: StopService-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 720895f72a69504eb2efafe24fc5a3e18005356f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111168"
---
# <a name="stopservice-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="6de98-103">StopService-Methode der Msvm \_ TerminalService-Klasse</span><span class="sxs-lookup"><span data-stu-id="6de98-103">StopService method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="6de98-104">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="6de98-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de98-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6de98-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="6de98-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6de98-106">Parameters</span></span>

<span data-ttu-id="6de98-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6de98-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6de98-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6de98-108">Return value</span></span>

<span data-ttu-id="6de98-109">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="6de98-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6de98-110">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6de98-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6de98-111">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6de98-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6de98-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de98-112">Requirements</span></span>



| <span data-ttu-id="6de98-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de98-113">Requirement</span></span> | <span data-ttu-id="6de98-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6de98-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de98-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6de98-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6de98-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6de98-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6de98-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6de98-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6de98-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6de98-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6de98-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="6de98-119">Namespace</span></span><br/>                | <span data-ttu-id="6de98-120">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6de98-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6de98-121">MOF</span><span class="sxs-lookup"><span data-stu-id="6de98-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6de98-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6de98-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6de98-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6de98-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de98-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6de98-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6de98-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6de98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de98-126">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="6de98-126">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




