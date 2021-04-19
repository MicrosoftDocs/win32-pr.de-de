---
description: Die PF \_ parserinfo-Struktur definiert jeweils einen Parser. In der PF \_ parserinfo-Struktur wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: PF_PARSERINFO Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348130"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="48156-104">PF- \_ parameserinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="48156-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="48156-105">Die **PF \_ parserinfo** -Struktur definiert jeweils einen Parser.</span><span class="sxs-lookup"><span data-stu-id="48156-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="48156-106">In der **PF \_ parserinfo** -Struktur wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.</span><span class="sxs-lookup"><span data-stu-id="48156-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="48156-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48156-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="48156-108">Member</span><span class="sxs-lookup"><span data-stu-id="48156-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="48156-109">**szprotocolname**</span><span class="sxs-lookup"><span data-stu-id="48156-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="48156-110">Der Name des Protokolls, das vom Parser erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="48156-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="48156-111">**szcomment**</span><span class="sxs-lookup"><span data-stu-id="48156-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="48156-112">Kurze Beschreibung des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="48156-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="48156-113">**szhelpfile**</span><span class="sxs-lookup"><span data-stu-id="48156-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="48156-114">Der Name der protokollhilfe Datei (falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="48156-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="48156-115">**pwhocanvoran**</span><span class="sxs-lookup"><span data-stu-id="48156-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="48156-116">Zeiger auf eine [PF \_](pf-followset.md) -nach Verfolgungs Struktur, die die Protokolle auflistet, die dem Protokoll vorangestellt sind, das die PF-Parameter **\_ Info** -Struktur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="48156-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="48156-117">Netzwerkmonitor fügt dem [*folgenden Satz*](f.md) aller Protokolle im Satz das parserprotokoll hinzu.</span><span class="sxs-lookup"><span data-stu-id="48156-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="48156-118">**pwhocanfollowme**</span><span class="sxs-lookup"><span data-stu-id="48156-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="48156-119">Zeiger auf eine [PF \_](pf-followset.md) -nach Verfolgungs Struktur, die das Protokoll auflistet, das dem Protokoll entsprechen kann, das von der PF-Parameter **\_ Info** -Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="48156-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="48156-120">Netzwerkmonitor fügt die Protokolle des Satzes dem [*folgenden Satz*](f.md) des parserprotokolls hinzu.</span><span class="sxs-lookup"><span data-stu-id="48156-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="48156-121">**pwhohandsofftome**</span><span class="sxs-lookup"><span data-stu-id="48156-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="48156-122">Zeiger auf eine [PF- \_ handoffset](pf-handoffset.md) -Struktur, die an das Protokoll übergibt, das von der PF-Parameter **\_ Info** -Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="48156-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="48156-123">Netzwerkmonitor fügt das parserprotokoll den [*Übergabe Sätzen*](h.md) aller Protokolle in der Menge hinzu.</span><span class="sxs-lookup"><span data-stu-id="48156-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="48156-124">**pwhodoihandoffto**</span><span class="sxs-lookup"><span data-stu-id="48156-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="48156-125">Zeiger auf eine [PF- \_ handoffset](pf-handoffset.md) -Struktur, die die Protokolle auflistet, an die das Parser-Protokoll übergibt.</span><span class="sxs-lookup"><span data-stu-id="48156-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="48156-126">Netzwerkmonitor fügt die Protokolle dieses Satzes dem [*Übergabe Satz*](h.md) des parserprotokolls hinzu.</span><span class="sxs-lookup"><span data-stu-id="48156-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48156-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48156-127">Remarks</span></span>

<span data-ttu-id="48156-128">Die **PF \_ parserinfo** -Struktur wird in der **PF \_ parserdllinfo** -Struktur verwendet, um eine Beschreibung eines Parsers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="48156-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="48156-129">Netzwerkmonitor verwendet die parserbeschreibung, um die [*Parser.ini*](p.md) Datei zu aktualisieren, und die INI-Dateien der Parser, die vor dem in der **PF \_ parserinfo** -Struktur beschriebenen Protokoll stehen.</span><span class="sxs-lookup"><span data-stu-id="48156-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="48156-130">Ein nachfolgenden Satz gibt die Protokolle an, die einem Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="48156-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="48156-131">Netzwerkmonitor verwendet einen nachfolgenden Satz, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz nicht identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="48156-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="48156-132">Ein nachfolgenden Satz wird in der [*Parser.ini*](p.md) -Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48156-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="48156-133">Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den folgenden Satz der parserprotokolle, die in " **pwhocanvoranstellen** " und " **pwhocanfollowme**" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="48156-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="48156-134">Ein Übergabe-Satz gibt die Protokolle an, die einem Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="48156-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="48156-135">Der Parser verwendet einen Handzettel Satz nur dann, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="48156-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="48156-136">Ein Übergabe-Satz wird in den INI-Dateien der einzelnen Parser gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48156-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="48156-137">Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den Übergabe Satz der parserprotokolle, die in **pwhohandsofftome** und **pwhodoihandoffto** aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="48156-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="48156-138">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="48156-138">For information on</span></span>                                               | <span data-ttu-id="48156-139">Siehe</span><span class="sxs-lookup"><span data-stu-id="48156-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="48156-140">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="48156-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="48156-141">Parser</span><span class="sxs-lookup"><span data-stu-id="48156-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="48156-142">Die folgenden Sätze enthalten.</span><span class="sxs-lookup"><span data-stu-id="48156-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="48156-143">Angeben eines folgenden Satzes</span><span class="sxs-lookup"><span data-stu-id="48156-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="48156-144">Gibt an, welche Handzettel Sätze enthalten.</span><span class="sxs-lookup"><span data-stu-id="48156-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="48156-145">Angeben einer Übergabe Gruppe</span><span class="sxs-lookup"><span data-stu-id="48156-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="48156-146">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48156-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="48156-147">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="48156-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="48156-148">Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="48156-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="48156-149">Implementieren von "parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="48156-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="48156-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48156-150">Requirements</span></span>



| <span data-ttu-id="48156-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48156-151">Requirement</span></span> | <span data-ttu-id="48156-152">Wert</span><span class="sxs-lookup"><span data-stu-id="48156-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48156-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48156-153">Minimum supported client</span></span><br/> | <span data-ttu-id="48156-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48156-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="48156-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48156-155">Minimum supported server</span></span><br/> | <span data-ttu-id="48156-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48156-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48156-157">Header</span><span class="sxs-lookup"><span data-stu-id="48156-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="48156-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="48156-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48156-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48156-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48156-160">"Parameserautoinstallinfo"</span><span class="sxs-lookup"><span data-stu-id="48156-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="48156-161">PF-nach \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="48156-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="48156-162">PF- \_ handoffset</span><span class="sxs-lookup"><span data-stu-id="48156-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="48156-163">PF- \_ Parser (Parser)</span><span class="sxs-lookup"><span data-stu-id="48156-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




