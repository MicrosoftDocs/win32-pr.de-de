---
description: Die entryPoints-Struktur definiert die Einstiegspunkte für die Exportfunktionen, die von Netzwerkmonitor zum Ausführen des Parsers verwendet werden.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: EntryPoints-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958732"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="fda21-103">EntryPoints-Struktur</span><span class="sxs-lookup"><span data-stu-id="fda21-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="fda21-104">Die **entryPoints** -Struktur definiert die Einstiegspunkte für die Exportfunktionen, die von Netzwerkmonitor zum Ausführen des Parsers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fda21-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fda21-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="fda21-106">Member</span><span class="sxs-lookup"><span data-stu-id="fda21-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fda21-107">**Registrieren**</span><span class="sxs-lookup"><span data-stu-id="fda21-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="fda21-108">Ein Zeiger auf die Implementierung der [*Register-expertenfunktion*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="fda21-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fda21-109">**Registrierung aufheben**</span><span class="sxs-lookup"><span data-stu-id="fda21-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="fda21-110">Ein Zeiger auf die Implementierung der [**deregiester**](deregister.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fda21-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fda21-111">**Erkenzeframe**</span><span class="sxs-lookup"><span data-stu-id="fda21-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="fda21-112">Ein Zeiger auf die Implementierung der Funktion " [**Erkennungs Frame**](recognizeframe.md) -Export".</span><span class="sxs-lookup"><span data-stu-id="fda21-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="fda21-113">**Attachproperties**</span><span class="sxs-lookup"><span data-stu-id="fda21-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="fda21-114">Ein Zeiger auf die Implementierung der " [**attachproperties**](attachproperties.md) "-Exportfunktion.</span><span class="sxs-lookup"><span data-stu-id="fda21-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="fda21-115">**Formatproperties**</span><span class="sxs-lookup"><span data-stu-id="fda21-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="fda21-116">Ein Zeiger auf die Implementierung der [**formatproperties**](formatproperties.md) -Exportfunktion.</span><span class="sxs-lookup"><span data-stu-id="fda21-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fda21-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fda21-117">Remarks</span></span>

<span data-ttu-id="fda21-118">Die **Funktion "** **entryPoints" verwendet die entryPoints** -Struktur, um Zeiger auf Netzwerkmonitor bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fda21-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="fda21-119">Die Zeiger müssen in der im vorherigen Members-Abschnitt identifizierten Reihenfolge angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fda21-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="fda21-120">Die [**formatproperties**](formatproperties.md) -Funktion muss nicht implementiert werden, wenn Netzwerkmonitor die Protokolldaten niemals anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fda21-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="fda21-121">Beispielsweise muss **formatproperties** nicht implementiert werden, wenn eine Export Anwendung die Ausgabe des Parsers verwendet und Netzwerkmonitor die Ausgabe nicht anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fda21-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="fda21-122">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="fda21-122">For information on</span></span>                                        | <span data-ttu-id="fda21-123">Siehe</span><span class="sxs-lookup"><span data-stu-id="fda21-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fda21-124">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fda21-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="fda21-125">Parser</span><span class="sxs-lookup"><span data-stu-id="fda21-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="fda21-126">Zur Implementierung von **DllMain**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="fda21-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="fda21-127">Implementieren von DllMain</span><span class="sxs-lookup"><span data-stu-id="fda21-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="fda21-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fda21-128">Requirements</span></span>



| <span data-ttu-id="fda21-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fda21-129">Requirement</span></span> | <span data-ttu-id="fda21-130">Wert</span><span class="sxs-lookup"><span data-stu-id="fda21-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fda21-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fda21-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fda21-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fda21-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fda21-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fda21-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fda21-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fda21-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fda21-135">Header</span><span class="sxs-lookup"><span data-stu-id="fda21-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda21-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fda21-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fda21-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fda21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda21-138">Attachproperties</span><span class="sxs-lookup"><span data-stu-id="fda21-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="fda21-139">"Kreateprotocol"</span><span class="sxs-lookup"><span data-stu-id="fda21-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="fda21-140">Registrierung aufheben</span><span class="sxs-lookup"><span data-stu-id="fda21-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="fda21-141">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="fda21-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="fda21-142">Erkenzeframe</span><span class="sxs-lookup"><span data-stu-id="fda21-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="fda21-143">Registrieren</span><span class="sxs-lookup"><span data-stu-id="fda21-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




