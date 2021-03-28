---
description: Wird an eine Anwendung gesendet, die eine Schulungs Karte mit der Windows-Hilfe initiiert hat.
title: WM_TCARD Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215928"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="def6f-103">WM- \_ TCard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="def6f-103">WM\_TCARD message</span></span>

<span data-ttu-id="def6f-104">Wird an eine Anwendung gesendet, die eine Schulungs Karte mit der Windows-Hilfe initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="def6f-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="def6f-105">Die Meldung informiert die Anwendung, wenn der Benutzer auf eine Schaltfläche zum autorierbaren Klicken klickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="def6f-106">Eine Anwendung initiiert eine Schulungs Karte, indem Sie den Help \_ TCard-Befehl in einem aufzurufenden Befehl der [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="def6f-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="def6f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="def6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def6f-108">*idaction*</span><span class="sxs-lookup"><span data-stu-id="def6f-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="def6f-109">Ein-Wert, der die Aktion angibt, die der Benutzer ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="def6f-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="def6f-110">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="def6f-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="def6f-111"><span id="IDABORT"></span><span id="idabort"></span>**Idabort**</span><span class="sxs-lookup"><span data-stu-id="def6f-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-112">Der Benutzer hat auf eine autorilier Bare **Abbruch** Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="def6f-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="def6f-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-114">Der Benutzer hat auf eine autorilier Bare Schaltfläche **Abbrechen** geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="def6f-115"><span id="IDCLOSE"></span><span id="idclose"></span>**Idclose**</span><span class="sxs-lookup"><span data-stu-id="def6f-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-116">Der Benutzer hat die Schulungs Karte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="def6f-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="def6f-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="def6f-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-118">Der Benutzer hat auf eine autorisierte Windows- **Hilfe** Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="def6f-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="def6f-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-120">Der Benutzer hat auf eine autorilier Bare Schaltfläche **ignorieren** geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="def6f-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="def6f-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-122">Der Benutzer hat auf eine autorilier Bare Schaltfläche **OK** geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="def6f-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="def6f-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-124">Der Benutzer hat auf eine autorilier Bare **No** -Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="def6f-125"><span id="IDRETRY"></span><span id="idretry"></span>**Idretry**</span><span class="sxs-lookup"><span data-stu-id="def6f-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-126">Der Benutzer hat auf eine autorilier Bare **Wiederholungs** Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="def6f-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Unterstützung von \_ TCard- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="def6f-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-128">Der Benutzer hat auf eine autorilier Bare Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-128">The user clicked an authorable button.</span></span> <span data-ttu-id="def6f-129">Der *dwaktiondata* -Parameter enthält eine lange Ganzzahl, die vom Hilfe Autor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="def6f-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="def6f-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Help \_ TCard \_ other \_ Caller**</span><span class="sxs-lookup"><span data-stu-id="def6f-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-131">Eine andere Anwendung hat Trainingskarten angefordert.</span><span class="sxs-lookup"><span data-stu-id="def6f-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="def6f-132"><span id="IDYES"></span><span id="idyes"></span>**Idylle**</span><span class="sxs-lookup"><span data-stu-id="def6f-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="def6f-133">Der Benutzer hat auf eine autorilier Bare **Ja** -Schaltfläche geklickt.</span><span class="sxs-lookup"><span data-stu-id="def6f-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="def6f-134">*dwaktiondata*</span><span class="sxs-lookup"><span data-stu-id="def6f-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="def6f-135">Wenn *idaction* Hilfe- \_ TCard- \_ Daten angibt, wird dieser Parameter vom Hilfe Autor **lange** angegeben.</span><span class="sxs-lookup"><span data-stu-id="def6f-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="def6f-136">Andernfalls ist dieser Parameter gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="def6f-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def6f-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="def6f-137">Return value</span></span>

<span data-ttu-id="def6f-138">Der Rückgabewert wird ignoriert. NULL verwenden.</span><span class="sxs-lookup"><span data-stu-id="def6f-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="def6f-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="def6f-139">Requirements</span></span>



| <span data-ttu-id="def6f-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="def6f-140">Requirement</span></span> | <span data-ttu-id="def6f-141">Wert</span><span class="sxs-lookup"><span data-stu-id="def6f-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="def6f-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="def6f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="def6f-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="def6f-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="def6f-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="def6f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="def6f-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="def6f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="def6f-146">Header</span><span class="sxs-lookup"><span data-stu-id="def6f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="def6f-147"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="def6f-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




