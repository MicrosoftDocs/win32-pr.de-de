---
description: Die linetranslateresult \_ -bitflagkonstanten beschreiben verschiedene Ergebnisse einer Adressübersetzung.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: LINETRANSLATERESULT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354829"
---
# <a name="linetranslateresult_-constants"></a><span data-ttu-id="21b72-103">Linetranslateresult- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="21b72-103">LINETRANSLATERESULT\_ Constants</span></span>

<span data-ttu-id="21b72-104">Die **linetranslateresult \_** -bitflagkonstanten beschreiben verschiedene Ergebnisse einer Adressübersetzung.</span><span class="sxs-lookup"><span data-stu-id="21b72-104">The **LINETRANSLATERESULT\_** bit-flag constants describe various results of an address translation.</span></span>

<dl> <dt>

<span data-ttu-id="21b72-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**linetranslateresult \_ Canonical**</span><span class="sxs-lookup"><span data-stu-id="21b72-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT\_CANONICAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-106">Gibt an, dass die Eingabe Zeichenfolge ein gültiges kanonisches Format hat.</span><span class="sxs-lookup"><span data-stu-id="21b72-106">Indicates that the input string was in valid canonical format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**linetranslateresult \_ dialbilling**</span><span class="sxs-lookup"><span data-stu-id="21b72-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-108">Gibt an, dass die zurückgegebene Adresse ein "$" enthält.</span><span class="sxs-lookup"><span data-stu-id="21b72-108">Indicates that the returned address contains a "$".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**linetranslateresult \_ dialdialtone**</span><span class="sxs-lookup"><span data-stu-id="21b72-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-110">Gibt an, dass die zurückgegebene Adresse ein "W" enthält.</span><span class="sxs-lookup"><span data-stu-id="21b72-110">Indicates that the returned address contains a "W".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**linetranslateresult- \_ dialprompt**</span><span class="sxs-lookup"><span data-stu-id="21b72-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-112">Gibt an, dass die zurückgegebene Adresse ein "?" enthält.</span><span class="sxs-lookup"><span data-stu-id="21b72-112">Indicates that the returned address contains a "?".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**linetranslateresult \_ dialquiet**</span><span class="sxs-lookup"><span data-stu-id="21b72-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-114">Gibt an, dass die zurückgegebene Adresse ein @-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="21b72-114">Indicates that the returned address contain a "@".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**linetranslateresult \_ International**</span><span class="sxs-lookup"><span data-stu-id="21b72-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT\_INTERNATIONAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-116">Gibt an, dass der-Befehl als internationaler-Rückruf behandelt wird (der in der Zieladresse angegebene Landes-oder Regions Code unterscheidet sich von dem für **currentlocation** angegebenen Länder-oder Regions Code).</span><span class="sxs-lookup"><span data-stu-id="21b72-116">Indicates that the call is being treated as an international call (country or region code specified in the destination address is different from the country or region code specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**linetranslateresult \_ intolllist**</span><span class="sxs-lookup"><span data-stu-id="21b72-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT\_INTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-118">Gibt an, dass der lokale Aufruf als lange Distanz gewählt wird, da für das Land oder die Region Maut Anrufe festgestellt werden und das Präfix in der **tollprefixlist** von **currentlocation** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="21b72-118">Indicates that the local call is being dialed as long distance because the country or region has toll calling and the prefix appears in the **TollPrefixList** of the **CurrentLocation**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**linetranslateresult \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="21b72-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-120">Gibt an, dass der-Befehl als lokaler-Befehl behandelt wird (Land-oder Regions Code und in der Zieladresse angegebener Bereichs Code entsprechen denen, die für **currentlocation** angegeben sind).</span><span class="sxs-lookup"><span data-stu-id="21b72-120">Indicates that the call is being treated as a local call (country or region code and area code specified in the destination address are the same as those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**linetranslateresult \_ Longdistance**</span><span class="sxs-lookup"><span data-stu-id="21b72-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT\_LONGDISTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-122">Gibt an, dass der-Befehl als langer Entfernungs Rückruf behandelt wird (der in der Zieladresse angegebene Landes-oder Regions Code ist identisch, aber der flächencode unterscheidet sich von dem, der für **currentlocation** angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="21b72-122">Indicates that the call is being treated as a long distance call (country or region code specified in the destination address is the same but area code is different from those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**linetranslateresult \_ notintolllist**</span><span class="sxs-lookup"><span data-stu-id="21b72-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT\_NOTINTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-124">Gibt an, dass das Land oder die Region Maut Anrufe unterstützt, das Präfix aber nicht in der **tollprefixlist** angezeigt wird, sodass der Aufruf als lokaler Aufruf gewählt wird.</span><span class="sxs-lookup"><span data-stu-id="21b72-124">Indicates that the country or region supports toll calling but the prefix does not appear in the **TollPrefixList**, so the call is dialed as a local call.</span></span> <span data-ttu-id="21b72-125">Beachten Sie Folgendes: Wenn sowohl intollist als auch notintollist deaktiviert sind, unterstützt das aktuelle Land oder die Region keine Maut Präfixe, und Benutzeroberflächen Elemente im Zusammenhang mit Maut Präfixen sollten dem Benutzer nicht angezeigt werden. Wenn ein solches Bit aktiviert ist, unterstützt das Land oder die Region Maut Listen, und die zugehörigen Benutzeroberflächen Elemente sollten aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="21b72-125">Note that if both INTOLLIST and NOTINTOLLIST are off, the current country or region does not support toll prefixes, and user-interface elements related to toll prefixes should not be presented to the user; if either such bit is on, the country or region does support toll lists, and the related user-interface elements should be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**linetranslateresult \_ notranslation**</span><span class="sxs-lookup"><span data-stu-id="21b72-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT\_NOTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-127">Gibt an, dass die Adressübersetzung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="21b72-127">Indicates that address translation is not available.</span></span> <span data-ttu-id="21b72-128">Dieses Element ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="21b72-128">This element is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21b72-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**linetranslateresult \_ voicedetect**</span><span class="sxs-lookup"><span data-stu-id="21b72-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT\_VOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21b72-130">Gibt an, dass die zurückgegebene, als nicht zulässig angegebene Adresse ein ":" enthält.</span><span class="sxs-lookup"><span data-stu-id="21b72-130">Indicates that the returned dialable address contains a ":".</span></span> <span data-ttu-id="21b72-131">Dieses Element ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="21b72-131">This element is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>

> [!Note]  
> <span data-ttu-id="21b72-132">Das Zeichen ":" (Doppelpunkt) wird der Liste der Zeichen hinzugefügt, die in eine ddable-Zeichenfolge eingebettet und an Zieladressen übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="21b72-132">The ":" (colon) character will be added to the list of characters that can be embedded in a dialable string and passed into destination addresses.</span></span> <span data-ttu-id="21b72-133">Der Versuch, es von einer Anwendung an ein Line-Gerät zu übergeben, das eine API-Version vor 2,0 unterstützt, führt wahrscheinlich zu lineerr \_ invaladdress oder möglicherweise in dem Zeichen, das vollständig ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="21b72-133">Attempting to pass it from an application to a line device that supports an API version earlier than 2.0 will most likely result in LINEERR\_INVALADDRESS, or possibly in the character being ignored entirely.</span></span> <span data-ttu-id="21b72-134">Die Bedeutung dieses Zeichens ist "anhalten, bis eine Spracheingabe Aufforderung erkannt wird. Es ist für die Verwendung bei der automatischen Wahl von Systemen vorgesehen, die Spracheingabe Aufforderungen wie z. b. lange Entfernungs Karten Prozessoren zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="21b72-134">The meaning of this character is "Pause until a voice prompt is detected, then continue dialing"; it is intended for use when automatically dialing into systems that give voice prompts, such as long distance calling card processors.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21b72-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21b72-135">Remarks</span></span>

<span data-ttu-id="21b72-136">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="21b72-136">No extensibility.</span></span> <span data-ttu-id="21b72-137">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="21b72-137">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b72-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21b72-138">Requirements</span></span>



| <span data-ttu-id="21b72-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21b72-139">Requirement</span></span> | <span data-ttu-id="21b72-140">Wert</span><span class="sxs-lookup"><span data-stu-id="21b72-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="21b72-141">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="21b72-141">TAPI version</span></span><br/> | <span data-ttu-id="21b72-142">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="21b72-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="21b72-143">Header</span><span class="sxs-lookup"><span data-stu-id="21b72-143">Header</span></span><br/>       | <dl> <span data-ttu-id="21b72-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="21b72-144"><dt>Tapi.h</dt></span></span> </dl> |



 

 




