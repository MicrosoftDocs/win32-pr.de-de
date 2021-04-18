---
description: Die Register Export-Funktion muss in allen Parser-DLLs implementiert werden. Die Implementierung von Register erstellt und füllt eine Eigenschaften Datenbank für ein Protokoll aus. Netzwerkmonitor verwendet die-Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Parser-Rückruffunktion registrieren (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347921"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="3d5c5-105">Parser-Rückruffunktion registrieren</span><span class="sxs-lookup"><span data-stu-id="3d5c5-105">Register Parser callback function</span></span>

<span data-ttu-id="3d5c5-106">Die **Register** Export-Funktion muss in allen Parser-DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="3d5c5-107">Die Implementierung von **Register** erstellt und füllt eine [*Eigenschaften Datenbank*](p.md) für ein Protokoll aus.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="3d5c5-108">Netzwerkmonitor verwendet die-Datenbank, um zu bestimmen, welche Eigenschaften das Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5c5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d5c5-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="3d5c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d5c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5c5-111">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d5c5-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d5c5-112">Das Handle des Protokolls, das Netzwerkmonitor beim Aufrufen von **Register** bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="3d5c5-113">Das *hprotocol* -Handle wird benötigt, wenn Export-Hilfsfunktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d5c5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d5c5-114">Return value</span></span>

<span data-ttu-id="3d5c5-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d5c5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d5c5-116">Remarks</span></span>

<span data-ttu-id="3d5c5-117">Netzwerkmonitor beginnt den Aufruf der **Register** Funktion, sobald eine Erfassung geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="3d5c5-118">Netzwerkmonitor Ruft die **Register** -Funktion für jedes Protokoll auf, das Sie identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="3d5c5-119">Die Funktion "-Funktion" übergibt einen Zeiger an die **Register** [-Funktion.](createprotocol.md)</span><span class="sxs-lookup"><span data-stu-id="3d5c5-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="3d5c5-120">Die Implementierung von **Register** umfasst Aufrufe der folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="3d5c5-121">Ein Aufrufen der Funktionen " [deatepropertydatabase](createpropertydatabase.md) " und " [AddProperty](/previous-versions/bb251873(v=msdn.10)) " zum Erstellen einer Datenbank mit allen Eigenschaften, die das Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="3d5c5-122">Wenn für das Protokoll ein [*Übergabe-Satz*](h.md)verwendet wird, ist ein Aufrufen der Funktion "| [atehandofftable](createhandofftable.md) " erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="3d5c5-123">Wenn die Parser-DLL mehrere Parser enthält und der Parser mehr als ein Protokoll erkennen kann, müssen Sie eine **Register** -Funktion für jedes Protokoll implementieren.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="3d5c5-124">Informationen zu</span><span class="sxs-lookup"><span data-stu-id="3d5c5-124">For Information on</span></span>                                        | <span data-ttu-id="3d5c5-125">Siehe</span><span class="sxs-lookup"><span data-stu-id="3d5c5-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="3d5c5-126">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="3d5c5-127">Parser</span><span class="sxs-lookup"><span data-stu-id="3d5c5-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="3d5c5-128">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="3d5c5-129">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="3d5c5-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="3d5c5-130">Zum Implementieren von **Register**  ist ein Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d5c5-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="3d5c5-131">Implementieren von Register</span><span class="sxs-lookup"><span data-stu-id="3d5c5-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="3d5c5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d5c5-132">Requirements</span></span>



| <span data-ttu-id="3d5c5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d5c5-133">Requirement</span></span> | <span data-ttu-id="3d5c5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="3d5c5-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5c5-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d5c5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5c5-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d5c5-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3d5c5-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d5c5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5c5-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d5c5-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d5c5-139">Header</span><span class="sxs-lookup"><span data-stu-id="3d5c5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5c5-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5c5-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5c5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d5c5-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d5c5-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3d5c5-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="3d5c5-143">"Kreatehandofftable"</span><span class="sxs-lookup"><span data-stu-id="3d5c5-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="3d5c5-144">"Kreatepropertydatabase"</span><span class="sxs-lookup"><span data-stu-id="3d5c5-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="3d5c5-145">"Kreateprotocol"</span><span class="sxs-lookup"><span data-stu-id="3d5c5-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

