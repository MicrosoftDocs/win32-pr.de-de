---
description: Die Funktion "destroyprotocol" zerstört das Protokoll, das von der Funktion "kreateprotocol" erstellt wird.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Destroyprotocol-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215888"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="bacf5-103">Destroyprotocol-Funktion</span><span class="sxs-lookup"><span data-stu-id="bacf5-103">DestroyProtocol function</span></span>

<span data-ttu-id="bacf5-104">Die Funktion " **destroyprotocol** " zerstört das Protokoll, das von der Funktion " **kreateprotocol** " erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bacf5-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bacf5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bacf5-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="bacf5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bacf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bacf5-107">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bacf5-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bacf5-108">Handle für das Protokoll, das zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="bacf5-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bacf5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bacf5-109">Return value</span></span>

<span data-ttu-id="bacf5-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="bacf5-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bacf5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bacf5-111">Remarks</span></span>

<span data-ttu-id="bacf5-112">Die Parser-DLL ruft die **destroyprotocol** -Funktion während der Implementierung von [DllMain](dllmain-parser.md)auf.</span><span class="sxs-lookup"><span data-stu-id="bacf5-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="bacf5-113">**Destroyprotocol** wird aufgerufen, wenn das Betriebssystem die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="bacf5-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="bacf5-114">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="bacf5-114">For information on</span></span>                                        | <span data-ttu-id="bacf5-115">Siehe</span><span class="sxs-lookup"><span data-stu-id="bacf5-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bacf5-116">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bacf5-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="bacf5-117">Parser</span><span class="sxs-lookup"><span data-stu-id="bacf5-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="bacf5-118">Zur Implementierung von **DllMain** gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="bacf5-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="bacf5-119">Implementieren von DllMain</span><span class="sxs-lookup"><span data-stu-id="bacf5-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="bacf5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bacf5-120">Requirements</span></span>



| <span data-ttu-id="bacf5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bacf5-121">Requirement</span></span> | <span data-ttu-id="bacf5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bacf5-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bacf5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bacf5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bacf5-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bacf5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bacf5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bacf5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bacf5-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bacf5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bacf5-127">Header</span><span class="sxs-lookup"><span data-stu-id="bacf5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bacf5-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bacf5-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bacf5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bacf5-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bacf5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bacf5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bacf5-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bacf5-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bacf5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bacf5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bacf5-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="bacf5-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




