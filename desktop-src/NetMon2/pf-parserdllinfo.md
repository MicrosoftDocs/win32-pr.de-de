---
description: Die PF \_ parserdllinfo-Struktur definiert die Parser, die sich in der Parser-DLL befinden.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: PF_PARSERDLLINFO Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960143"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="a8406-103">PF- \_ parameserdllinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="a8406-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="a8406-104">Die **PF \_ parserdllinfo** -Struktur definiert die Parser, die sich in der Parser-DLL befinden.</span><span class="sxs-lookup"><span data-stu-id="a8406-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8406-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="a8406-106">Member</span><span class="sxs-lookup"><span data-stu-id="a8406-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8406-107">**nparser**</span><span class="sxs-lookup"><span data-stu-id="a8406-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="a8406-108">Anzahl der Parser in der Parser-DLL.</span><span class="sxs-lookup"><span data-stu-id="a8406-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="a8406-109">**"Parser Info"**</span><span class="sxs-lookup"><span data-stu-id="a8406-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a8406-110">Array von [PF \_ parserinfo](pf-parserinfo.md) -Strukturen, die jeden Parser in der Parser-DLL beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a8406-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8406-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8406-111">Remarks</span></span>

<span data-ttu-id="a8406-112">Die **PF \_ parserdllinfo** -Struktur wird von der [parserautoinstallinfo](parserautoinstallinfo.md) -Exportfunktion zurückgegeben, die in der Parser-DLL implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="a8406-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="a8406-113">Die **parserautoinstallinfo** -Funktion identifiziert die Anzahl der Parser in der dll und verwendet ein Array von [PF \_ parserinfo](pf-parserinfo.md) -Strukturen, um die einzelnen Parser zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a8406-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="a8406-114">Die PF \_ parserdllinfo-Struktur muss mithilfe von **heapzuc** zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a8406-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="a8406-115">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="a8406-115">For information on</span></span>                                               | <span data-ttu-id="a8406-116">Siehe</span><span class="sxs-lookup"><span data-stu-id="a8406-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a8406-117">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a8406-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="a8406-118">Parser</span><span class="sxs-lookup"><span data-stu-id="a8406-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="a8406-119">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a8406-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="a8406-120">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="a8406-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="a8406-121">Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8406-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="a8406-122">Implementieren von "Parser autoistallinfo"</span><span class="sxs-lookup"><span data-stu-id="a8406-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="a8406-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8406-123">Requirements</span></span>



| <span data-ttu-id="a8406-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8406-124">Requirement</span></span> | <span data-ttu-id="a8406-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a8406-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8406-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8406-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a8406-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8406-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a8406-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8406-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a8406-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8406-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8406-130">Header</span><span class="sxs-lookup"><span data-stu-id="a8406-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8406-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8406-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8406-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8406-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8406-133">PF-Parameter \_ Info</span><span class="sxs-lookup"><span data-stu-id="a8406-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="a8406-134">"Parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="a8406-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




