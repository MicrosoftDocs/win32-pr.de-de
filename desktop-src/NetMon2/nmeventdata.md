---
description: Die nmeventdata-Struktur enthält Informationen zu einer Ereignis Bedingung, die an Netzwerkmonitor übermittelt wird, um eine Zeile in den expertenviewer einzufügen.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Nmeventdata-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863031"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="d1be1-103">Nmeventdata-Struktur</span><span class="sxs-lookup"><span data-stu-id="d1be1-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="d1be1-104">Die **nmeventdata** -Struktur enthält Informationen zu einer Ereignis Bedingung, die an Netzwerkmonitor übermittelt wird, um eine Zeile in den expertenviewer einzufügen.</span><span class="sxs-lookup"><span data-stu-id="d1be1-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1be1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1be1-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="d1be1-106">Member</span><span class="sxs-lookup"><span data-stu-id="d1be1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1be1-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="d1be1-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-108">Die Versionsnummer der **nmeventdata** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d1be1-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="d1be1-109">Die Versionsnummer muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d1be1-109">The version number must be zero.</span></span> <span data-ttu-id="d1be1-110">In zukünftigen Versionen von Netzwerkmonitor wird möglicherweise eine höhere Versionsnummer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-111">**Eventident**</span><span class="sxs-lookup"><span data-stu-id="d1be1-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-112">Bezeichner des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d1be1-112">Identifier of the event.</span></span> <span data-ttu-id="d1be1-113">**Eventident** ist für jeden Experten eindeutig und verweist auf eine [Ereignis Referenzseite](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="d1be1-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-114">**Flags**</span><span class="sxs-lookup"><span data-stu-id="d1be1-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-115">Ein Satz von Flags, der beschreibt, wer die Ereignisdaten sendet und wie das Ereignis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d1be1-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="d1be1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1be1-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="d1be1-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d1be1-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="d1be1-118"><dt>**\_ereignisflag- \_ Experte**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="d1be1-119">Das Ereignis stammt von einem Experten.</span><span class="sxs-lookup"><span data-stu-id="d1be1-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="d1be1-120"><dt>**nmeventflag \_ \_ zeigt keinen \_ \_ Schweregrad an**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="d1be1-121">Der Schweregrad für das Ereignis wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="d1be1-122"><dt>**nmeventflag \_ \_ keine \_ Quelle anzeigen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="d1be1-123">Der Quell Name für das Ereignis wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="d1be1-124"><dt>**nmeventflag \_ \_ zeigt den \_ \_ Ereignis \_ Namen nicht an**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="d1be1-125">Der Ereignis Name für das Ereignis wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="d1be1-126"><dt>**nmeventflag \_ \_ keine \_ Beschreibung anzeigen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="d1be1-127">Die Beschreibung für das Ereignis nicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d1be1-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="d1be1-128"><dt>**nmeventflag \_ keinen \_ \_ Computer anzeigen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="d1be1-129">Der Computername für das Ereignis wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="d1be1-130"><dt>**nmeventflag \_ \_ zeigt keine \_ \_ Zeit an**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="d1be1-131">Zeit für das Ereignis nicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="d1be1-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="d1be1-132"><dt>**"nmeventflag" \_ \_ \_ zeigt keine \_ festgelegten \_ Spalten an.**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="d1be1-133">Die Spalten Schweregrad, Quelle, Ereignis Name, Beschreibung, Computer oder Zeit werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="d1be1-134">Dabei handelt es sich nicht um ein einzelnes Flag, aber es handelt sich um eine Union der vorherigen sechs Flags.</span><span class="sxs-lookup"><span data-stu-id="d1be1-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="d1be1-135">**Severity**</span><span class="sxs-lookup"><span data-stu-id="d1be1-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-136">Schweregrad des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d1be1-136">Severity level of the event.</span></span> <span data-ttu-id="d1be1-137">Der Schweregrad kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d1be1-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="d1be1-138">nmevent \_ Schweregrad \_ Information nmevent \_ Schweregrad \_ Warnung nmevent \_ Schweregrad \_ Strong \_ Warnung nmevent \_ schwere \_ Fehler nmevent Schweregrad \_ \_ schwerwiegender Fehler \_ nmevent \_ Schweregrad \_ kritisch \_</span><span class="sxs-lookup"><span data-stu-id="d1be1-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="d1be1-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-140">Anzahl der in der aktuellen-Struktur bezeichneten Spalten.</span><span class="sxs-lookup"><span data-stu-id="d1be1-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-141">**szsourcename**</span><span class="sxs-lookup"><span data-stu-id="d1be1-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-142">Der Name des angezeigten Experten.</span><span class="sxs-lookup"><span data-stu-id="d1be1-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-143">**szeventname**</span><span class="sxs-lookup"><span data-stu-id="d1be1-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-144">Der Name des angezeigten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d1be1-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="d1be1-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-146">Die Beschreibung des angezeigten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d1be1-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-147">**szmachine**</span><span class="sxs-lookup"><span data-stu-id="d1be1-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-148">Veraltet, sollte **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d1be1-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-149">**Begründung**</span><span class="sxs-lookup"><span data-stu-id="d1be1-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-150">Informationen, die im zweiten Fenster der Ereignisanzeige angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1be1-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="d1be1-151">Der  ausrichtungmember kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d1be1-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="d1be1-152">Wenn der Wert **null** ist, ist das zweite Fenster nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d1be1-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-153">**szURL**</span><span class="sxs-lookup"><span data-stu-id="d1be1-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-154">Bleiben Dieser Member muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d1be1-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="d1be1-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-156">Der Zeitpunkt, zu dem die Ereignis Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="d1be1-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="d1be1-157">Die Zeit wird relativ zum Anfang der Erfassung gemessen.</span><span class="sxs-lookup"><span data-stu-id="d1be1-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="d1be1-158">**Spalte**</span><span class="sxs-lookup"><span data-stu-id="d1be1-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="d1be1-159">Tabelle mit Spalten Strukturen, die im oberen Bereich der Ereignisanzeige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d1be1-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1be1-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1be1-160">Requirements</span></span>



| <span data-ttu-id="d1be1-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1be1-161">Requirement</span></span> | <span data-ttu-id="d1be1-162">Wert</span><span class="sxs-lookup"><span data-stu-id="d1be1-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1be1-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1be1-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d1be1-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1be1-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d1be1-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1be1-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d1be1-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1be1-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1be1-167">Header</span><span class="sxs-lookup"><span data-stu-id="d1be1-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1be1-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1be1-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




