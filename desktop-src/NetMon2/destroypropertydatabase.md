---
description: Die Funktion "destroypropertydatabase" gibt die Ressourcen frei, die zum Erstellen der Protokoll Eigenschaften Datenbank verwendet werden.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Destroypropertydatabase-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960639"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="7e37a-103">Destroypropertydatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e37a-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="7e37a-104">Die Funktion " **destroypropertydatabase** " gibt die Ressourcen frei, die zum Erstellen der Protokoll [*Eigenschaften Datenbank*](p.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e37a-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e37a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e37a-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7e37a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e37a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e37a-107">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e37a-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e37a-108">Handle für die zu zerstörende Eigenschaften Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7e37a-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="7e37a-109">Das Handle wird an die Parser-DLL übergeben, wenn Netzwerkmonitor die [deregiester](deregister.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="7e37a-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e37a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e37a-110">Return value</span></span>

<span data-ttu-id="7e37a-111">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7e37a-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7e37a-112">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7e37a-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="7e37a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7e37a-113">Return code</span></span>                                                                                              | <span data-ttu-id="7e37a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e37a-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="7e37a-115"><dt>**Interner nmerr- \_ \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="7e37a-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="7e37a-116">Interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="7e37a-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="7e37a-117"><dt>**nmerr \_ ungültiges \_ hprotocol**</dt></span><span class="sxs-lookup"><span data-stu-id="7e37a-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="7e37a-118">Ungültiges Handle in *hprotocol*.</span><span class="sxs-lookup"><span data-stu-id="7e37a-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e37a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e37a-119">Remarks</span></span>

<span data-ttu-id="7e37a-120">Die **destroypropertydatabase** -Funktion sollte nur aufgerufen werden, wenn [die Funktion](deregister.md) zum Aufheben der Aufhebung des Registrierungs Diensts für das Protokoll implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7e37a-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="7e37a-121">Für Parser-DLLs, die mehrere Protokolle unterstützen, wird die Funktion " **destroypropertydatabase** " für jede Implementierung von " **deregiester**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7e37a-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="7e37a-122">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="7e37a-122">For information on</span></span>                                        | <span data-ttu-id="7e37a-123">Siehe</span><span class="sxs-lookup"><span data-stu-id="7e37a-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7e37a-124">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7e37a-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="7e37a-125">Parser</span><span class="sxs-lookup"><span data-stu-id="7e37a-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="7e37a-126">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7e37a-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="7e37a-127">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="7e37a-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="7e37a-128">Zum Implementieren der **deregiester**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7e37a-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="7e37a-129">Implementieren von deregistern</span><span class="sxs-lookup"><span data-stu-id="7e37a-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="7e37a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e37a-130">Requirements</span></span>



| <span data-ttu-id="7e37a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e37a-131">Requirement</span></span> | <span data-ttu-id="7e37a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7e37a-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7e37a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e37a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7e37a-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e37a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7e37a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e37a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7e37a-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e37a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7e37a-137">Header</span><span class="sxs-lookup"><span data-stu-id="7e37a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e37a-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e37a-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7e37a-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e37a-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e37a-140"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e37a-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7e37a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7e37a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e37a-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e37a-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e37a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e37a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e37a-144">Registrierung aufheben</span><span class="sxs-lookup"><span data-stu-id="7e37a-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




