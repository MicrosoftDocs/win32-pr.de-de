---
description: Die DllMain-Exportfunktion für den Parser identifiziert das vorhanden sein des Parsers und gibt Ressourcen frei, die von Netzwerkmonitor für den Parser verwendet werden. DllMain muss in allen Parser-DLLs implementiert werden.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: DllMain-Parser-Rückruffunktion (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360646"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="c71fb-104">DllMain-Parser-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="c71fb-104">DllMain Parser callback function</span></span>

<span data-ttu-id="c71fb-105">Die **DllMain** -Exportfunktion für den Parser identifiziert das vorhanden sein des Parsers und gibt Ressourcen frei, die von Netzwerkmonitor für den Parser verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c71fb-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="c71fb-106">**DllMain** muss in allen Parser-DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c71fb-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c71fb-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="c71fb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c71fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71fb-109">*HINSTANCE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c71fb-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71fb-110">Handle für eine Instanz des Parsers.</span><span class="sxs-lookup"><span data-stu-id="c71fb-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="c71fb-111">*Befehl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c71fb-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71fb-112">Indikator, um zu bestimmen, warum die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c71fb-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="c71fb-113">Eine Liste aller möglichen Flags finden Sie unter [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="c71fb-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="c71fb-114">Die Parser-Implementierung muss die folgenden Werte verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c71fb-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="c71fb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c71fb-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="c71fb-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c71fb-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="c71fb-117"><dt>**DLL- \_ Prozess \_ Anfügen**</dt></span><span class="sxs-lookup"><span data-stu-id="c71fb-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="c71fb-118">Wenn **DllMain** zum ersten Mal aufgerufen wird, muss die dll "up [Protocol](createprotocol.md) " aufrufen, um Informationen für Netzwerkmonitor bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c71fb-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="c71fb-119"><dt>**Trennen des DLL- \_ Prozesses \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c71fb-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="c71fb-120">Wenn **DllMain** zum letzten Mal aufgerufen wird, muss die DLL [destroyprotocol](destroyprotocol.md) aufrufen, um die von der dll verwendeten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c71fb-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c71fb-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="c71fb-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="c71fb-122">Wird jetzt nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c71fb-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71fb-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c71fb-123">Return value</span></span>

<span data-ttu-id="c71fb-124">Die Parser-DLL gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="c71fb-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c71fb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c71fb-125">Remarks</span></span>

<span data-ttu-id="c71fb-126">Das Betriebssystem ruft **DllMain** auf, um die Parser-DLL zu laden und zu entladen.</span><span class="sxs-lookup"><span data-stu-id="c71fb-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="c71fb-127">Diese Funktion basiert auf der [DllMain](/windows/desktop/Dlls/dllmain) -Funktion der Dynamic-Link Library.</span><span class="sxs-lookup"><span data-stu-id="c71fb-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="c71fb-128">Sie können auch die Implementierung von **DllMain** verwenden, um eine Instanz eines Parsers für die spätere Verwendung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c71fb-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="c71fb-129">Beispielsweise können Sie eine Parser-DLL-Instanz speichern und diese dann für einen System Aufrufvorgang in Zukunft verwenden.</span><span class="sxs-lookup"><span data-stu-id="c71fb-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="c71fb-130">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="c71fb-130">For information on</span></span>                                        | <span data-ttu-id="c71fb-131">Siehe</span><span class="sxs-lookup"><span data-stu-id="c71fb-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c71fb-132">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c71fb-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="c71fb-133">Parser</span><span class="sxs-lookup"><span data-stu-id="c71fb-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="c71fb-134">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c71fb-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="c71fb-135">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="c71fb-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="c71fb-136">Zur Implementierung von **DllMain**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c71fb-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="c71fb-137">Implementieren von DllMain</span><span class="sxs-lookup"><span data-stu-id="c71fb-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="c71fb-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c71fb-138">Requirements</span></span>



| <span data-ttu-id="c71fb-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c71fb-139">Requirement</span></span> | <span data-ttu-id="c71fb-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c71fb-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c71fb-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c71fb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c71fb-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c71fb-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c71fb-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c71fb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c71fb-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c71fb-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c71fb-145">Header</span><span class="sxs-lookup"><span data-stu-id="c71fb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71fb-146"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71fb-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71fb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c71fb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71fb-148">"Kreateprotocol"</span><span class="sxs-lookup"><span data-stu-id="c71fb-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="c71fb-149">Destroyprotocol</span><span class="sxs-lookup"><span data-stu-id="c71fb-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="c71fb-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="c71fb-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

