---
description: Mit der Funktion "-Funktion" wird Netzwerkmonitor benachrichtigt, dass ein bestimmter Protokoll Parser vorhanden ist.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Funktion "up Protocol" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131857"
---
# <a name="createprotocol-function"></a><span data-ttu-id="75065-103">Funktion "up Protocol"</span><span class="sxs-lookup"><span data-stu-id="75065-103">CreateProtocol function</span></span>

<span data-ttu-id="75065-104">Mit **der Funktion** "-Funktion" wird Netzwerkmonitor benachrichtigt, dass ein bestimmter Protokoll Parser vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="75065-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="75065-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75065-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="75065-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75065-107">*ProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75065-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75065-108">Der Name des Protokolls, das vom Parser erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="75065-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="75065-109">*lpentrypoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75065-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75065-110">Eine [entryPoints](entrypoints.md) -Struktur, die die verbleibenden Parser-DLL-Einstiegspunkte enthält.</span><span class="sxs-lookup"><span data-stu-id="75065-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="75065-111">In den Hinweisen finden Sie eine Liste der Exportfunktionen, auf die jeder Einstiegspunkt verweist.</span><span class="sxs-lookup"><span data-stu-id="75065-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="75065-112">Einstiegspunkte müssen in der Reihenfolge angegeben werden, in der die **entryPoints** -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="75065-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="75065-113">*cbentrypoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75065-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75065-114">Die Größe der **entryPoints** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="75065-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="75065-115">Netzwerkmonitor stellt ein Makro der entryPoints- \_ Größe bereit, mit dem Sie die Größe der Struktur angeben können.</span><span class="sxs-lookup"><span data-stu-id="75065-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75065-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75065-116">Return value</span></span>

<span data-ttu-id="75065-117">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="75065-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="75065-118">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="75065-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75065-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75065-119">Remarks</span></span>

<span data-ttu-id="75065-120">Die Parser-DLL ruft während der Implementierung von [DllMain](dllmain-parser.md)" **kreateprotocol** " auf.</span><span class="sxs-lookup"><span data-stu-id="75065-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="75065-121">Die **Funktion "** Funktion" wird aufgerufen, wenn das Betriebssystem die Parser-DLL zum ersten Mal lädt.</span><span class="sxs-lookup"><span data-stu-id="75065-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="75065-122">Die Einstiegspunkte, auf die im *lpentrypoints* -Parameter verwiesen wird, enthalten Verweise auf die folgenden Exportfunktionen, die in der hier dargestellten Reihenfolge bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="75065-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="75065-123">Registrieren</span><span class="sxs-lookup"><span data-stu-id="75065-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="75065-124">Registrierung aufheben</span><span class="sxs-lookup"><span data-stu-id="75065-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="75065-125">Erkenzeframe</span><span class="sxs-lookup"><span data-stu-id="75065-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="75065-126">Attachproperties</span><span class="sxs-lookup"><span data-stu-id="75065-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="75065-127">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="75065-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="75065-128">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="75065-128">For information on</span></span>                                                                                 | <span data-ttu-id="75065-129">Siehe</span><span class="sxs-lookup"><span data-stu-id="75065-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="75065-130">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="75065-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="75065-131">Parser</span><span class="sxs-lookup"><span data-stu-id="75065-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="75065-132">Zum Implementieren von **DllMain** ist ein Beispiel für das Aufrufen von **createprotocol** in **DllMain** enthalten.</span><span class="sxs-lookup"><span data-stu-id="75065-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="75065-133">Implementieren von DllMain</span><span class="sxs-lookup"><span data-stu-id="75065-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="75065-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75065-134">Requirements</span></span>



| <span data-ttu-id="75065-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75065-135">Requirement</span></span> | <span data-ttu-id="75065-136">Wert</span><span class="sxs-lookup"><span data-stu-id="75065-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75065-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75065-137">Minimum supported client</span></span><br/> | <span data-ttu-id="75065-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75065-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75065-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75065-139">Minimum supported server</span></span><br/> | <span data-ttu-id="75065-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75065-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75065-141">Header</span><span class="sxs-lookup"><span data-stu-id="75065-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="75065-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75065-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="75065-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75065-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="75065-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75065-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="75065-145">DLL</span><span class="sxs-lookup"><span data-stu-id="75065-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75065-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75065-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75065-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75065-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75065-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="75065-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

