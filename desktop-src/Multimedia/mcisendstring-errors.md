---
title: mciSendString-Fehler
description: mciSendString-Fehler
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Mcierr-Rückgabewerte, mciSendString-Fehler
- Multimedia-Referenz, mciSendString-Fehler
- Referenz für Multimedia-, mciSendString-Fehler
- MCI-Fehler (Media Control Interface), mciSendString-Fehler
- MCI (Media Control Interface), mciSendString-Fehler
- Referenz für MCI-, mciSendString-Fehler
- MCI-Referenz, mciSendString-Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- mciSendString-Fehler
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858216"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="1a00a-116">mciSendString-Fehler</span><span class="sxs-lookup"><span data-stu-id="1a00a-116">mciSendString Errors</span></span>

<span data-ttu-id="1a00a-117">Die folgenden Fehler werden von der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion, nicht jedoch von [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="1a00a-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="1a00a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1a00a-118">Value</span></span>                             | <span data-ttu-id="1a00a-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1a00a-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="1a00a-120">mcierr-ungültige \_ \_ Konstante</span><span class="sxs-lookup"><span data-stu-id="1a00a-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="1a00a-121">Der für einen Parameter angegebene Wert ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1a00a-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="1a00a-122">Ungültige mcierr- \_ \_ Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1a00a-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="1a00a-123">Eine ganze Zahl im Befehl war ungültig oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="1a00a-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="1a00a-124">doppelte mcierr- \_ \_ Flags</span><span class="sxs-lookup"><span data-stu-id="1a00a-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="1a00a-125">Ein Flag oder ein Wert wurde zweimal angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a00a-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="1a00a-126">\_fehlende \_ Befehls \_ Zeichenfolge für mcierr</span><span class="sxs-lookup"><span data-stu-id="1a00a-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="1a00a-127">Es wurde kein Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a00a-127">No command was specified.</span></span>                         |
| <span data-ttu-id="1a00a-128">mcierr \_ fehlt \_ Geräte \_ Name</span><span class="sxs-lookup"><span data-stu-id="1a00a-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="1a00a-129">Es wurde kein Gerätename angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a00a-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="1a00a-130">\_fehlendes Zeichen folgen \_ \_ Argument für mcierr</span><span class="sxs-lookup"><span data-stu-id="1a00a-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="1a00a-131">Im Befehl fehlte ein Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="1a00a-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="1a00a-132">mcierr \_ New \_ erfordert \_ Alias</span><span class="sxs-lookup"><span data-stu-id="1a00a-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="1a00a-133">Ein Alias muss mit dem Gerätenamen "New" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a00a-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="1a00a-134">mcierr \_ kein \_ Schließ Endes \_ Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="1a00a-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="1a00a-135">Ein Schließ Endes Anführungszeichen fehlt.</span><span class="sxs-lookup"><span data-stu-id="1a00a-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="1a00a-136">mcierr \_ \_ beim \_ automatischen \_ Öffnen Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="1a00a-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="1a00a-137">Das Flag "Benachrichtigen" ist mit dem automatischen öffnen unzulässig.</span><span class="sxs-lookup"><span data-stu-id="1a00a-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="1a00a-138">mcierr-Parameter \_ \_ Überlauf</span><span class="sxs-lookup"><span data-stu-id="1a00a-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="1a00a-139">Die Ausgabe Zeichenfolge war nicht lang genug.</span><span class="sxs-lookup"><span data-stu-id="1a00a-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="1a00a-140">Interner mcierr- \_ Parser \_</span><span class="sxs-lookup"><span data-stu-id="1a00a-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="1a00a-141">Interner Parserfehler.</span><span class="sxs-lookup"><span data-stu-id="1a00a-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="1a00a-142">Unbekanntes mcierr- \_ \_ Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="1a00a-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="1a00a-143">Es wurde ein unbekannter Befehlsparameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a00a-143">An unknown command parameter was specified.</span></span>       |



 

 

 