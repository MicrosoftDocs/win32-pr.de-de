---
description: Die parserautoinstallinfo-Exportfunktion identifiziert den Parser oder Parser, die sich in einer DLL befinden. Parserautoinstallinfo sollte in allen Parser-DLLs implementiert werden.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: "\"Parameserautoinstallinfo\"-Rückruffunktion (Netmon. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342739"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="162de-104">Parameserautoinstallinfo-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="162de-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="162de-105">Die **parserautoinstallinfo** -Exportfunktion identifiziert den Parser oder Parser, die sich in einer DLL befinden.</span><span class="sxs-lookup"><span data-stu-id="162de-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="162de-106">**Parserautoinstallinfo** sollte in allen Parser-DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="162de-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="162de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="162de-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="162de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="162de-108">Parameters</span></span>

<span data-ttu-id="162de-109">Diese Rückruffunktion hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="162de-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="162de-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="162de-110">Return value</span></span>

<span data-ttu-id="162de-111">Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine [PF- \_ parametedllinfo](pf-parserdllinfo.md) -Struktur, die die Parser in der dll beschreibt.</span><span class="sxs-lookup"><span data-stu-id="162de-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="162de-112">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="162de-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="162de-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="162de-113">Remarks</span></span>

<span data-ttu-id="162de-114">Wenn Netzwerkmonitor zum ersten Mal geladen wird, wird **parserautoinstallinfo** aufgerufen (sofern vorhanden), um jeden Parser automatisch zu installieren, und anschließend werden alle parserdlls im Parser-Unterverzeichnis aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="162de-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="162de-115">Zu den Informationen, die in der **PF-parametdllinfo \_** -Struktur zurückgegeben werden, gehören folgende:</span><span class="sxs-lookup"><span data-stu-id="162de-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="162de-116">Die Anzahl der Parser in der dll (in der Regel eine).</span><span class="sxs-lookup"><span data-stu-id="162de-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="162de-117">Der Name und eine kurze Beschreibung des Protokolls, das jeder Parser erkennt.</span><span class="sxs-lookup"><span data-stu-id="162de-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="162de-118">Eine optionale Hilfedatei für jedes Protokoll.</span><span class="sxs-lookup"><span data-stu-id="162de-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="162de-119">Die Protokolle, die jedem Protokoll vorangestellt sind.</span><span class="sxs-lookup"><span data-stu-id="162de-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="162de-120">Die Protokolle, die auf die einzelnen Protokolle folgen.</span><span class="sxs-lookup"><span data-stu-id="162de-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="162de-121">Jede Parser-DLL sollte einen Parser enthalten.</span><span class="sxs-lookup"><span data-stu-id="162de-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="162de-122">Netzwerkmonitor ermöglicht es Ihnen jedoch, eine DLL zu erstellen, die mehr als einen Parser enthält.</span><span class="sxs-lookup"><span data-stu-id="162de-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="162de-123">Beispielsweise ist tcpip.dll eine Netzwerkmonitor-dll mit mehr als einem Parser.</span><span class="sxs-lookup"><span data-stu-id="162de-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="162de-124">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="162de-124">For information on</span></span>                                               | <span data-ttu-id="162de-125">Siehe</span><span class="sxs-lookup"><span data-stu-id="162de-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="162de-126">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="162de-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="162de-127">Parser</span><span class="sxs-lookup"><span data-stu-id="162de-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="162de-128">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="162de-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="162de-129">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="162de-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="162de-130">Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="162de-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="162de-131">Implementieren von "parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="162de-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="162de-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="162de-132">Requirements</span></span>



| <span data-ttu-id="162de-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="162de-133">Requirement</span></span> | <span data-ttu-id="162de-134">Wert</span><span class="sxs-lookup"><span data-stu-id="162de-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="162de-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="162de-135">Minimum supported client</span></span><br/> | <span data-ttu-id="162de-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="162de-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="162de-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="162de-137">Minimum supported server</span></span><br/> | <span data-ttu-id="162de-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="162de-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="162de-139">Header</span><span class="sxs-lookup"><span data-stu-id="162de-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="162de-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="162de-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="162de-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="162de-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162de-142">PF- \_ Parser (Parser)</span><span class="sxs-lookup"><span data-stu-id="162de-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




