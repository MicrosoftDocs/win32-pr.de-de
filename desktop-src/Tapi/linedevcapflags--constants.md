---
description: Die \_ Bits-Flag-Konstanten von linedevcapflags sind eine Auflistung von booleschen Werten, in denen verschiedene Zeilen Gerätefunktionen beschrieben werden.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359794"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="d8b97-103">Linedevcapflags- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="d8b97-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="d8b97-104">Die Bits-Flag-Konstanten von **linedevcapflags \_** sind eine Auflistung von booleschen Werten, in denen verschiedene Zeilen Gerätefunktionen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="d8b97-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**linedevcapflags \_ callhub**</span><span class="sxs-lookup"><span data-stu-id="d8b97-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-106">Gibt an, ob callhubs in dieser Zeile unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="d8b97-107">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="d8b97-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**linedevcapflags \_ callhubtracking**</span><span class="sxs-lookup"><span data-stu-id="d8b97-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-109">Gibt an, ob die callhub-Nachverfolgung in dieser Zeile unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="d8b97-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="d8b97-110">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="d8b97-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**linedevcapflags- \_ closedrop**</span><span class="sxs-lookup"><span data-stu-id="d8b97-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-112">Gibt an, was geschieht, wenn eine geöffnete Zeile geschlossen wird, während die Anwendung Aufrufe aktiv in der Zeile ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d8b97-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="d8b97-113">**True** gibt an, dass der Dienstanbieter alle aktiven Aufrufe in der Zeile löscht (löscht), wenn die letzte Anwendung, die die Zeile geöffnet hat, mit [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d8b97-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="d8b97-114">**False** gibt an, dass der Dienstanbieter in solchen Fällen keine aktiven Aufrufe löscht.</span><span class="sxs-lookup"><span data-stu-id="d8b97-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="d8b97-115">Stattdessen bleiben die Aufrufe aktiv und Steuern externe Geräte.</span><span class="sxs-lookup"><span data-stu-id="d8b97-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="d8b97-116">Ein Dienstanbieter legt dieses Bit in der Regel auf " **false** " fest, wenn es ein anderes Gerät gibt, das den Anruf aufrechterhalten kann. Wenn z. b. eine analoge Linie den Computer aufweist und die Telefonnummer in einer Partei Konfiguration direkt mit Ihnen verbunden ist, hält das OFFHOOK-Telefon den Anruf automatisch an, selbst nachdem der Computer eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="d8b97-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="d8b97-117">Anwendungen sollten dieses Flag überprüfen, um zu bestimmen, ob der Benutzer gewarnt werden soll (im Dialogfeld OK/Abbrechen), dass aktive Aufrufe verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="d8b97-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**linedevcapflags \_ crossaddrconf**</span><span class="sxs-lookup"><span data-stu-id="d8b97-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-119">Gibt an, ob Aufrufe an verschiedene Adressen in dieser Zeile übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="d8b97-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**linedevcapflags- \_ dialabrechnung**</span><span class="sxs-lookup"><span data-stu-id="d8b97-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**linedevcapflags- \_ dialdialtone**</span><span class="sxs-lookup"><span data-stu-id="d8b97-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**linedevcapflags- \_ dialquiet**</span><span class="sxs-lookup"><span data-stu-id="d8b97-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-123">Diese Flags geben an, ob der deklarable String-Modifizierer "$", "@" oder "W" für ein bestimmtes Zeilen Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d8b97-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="d8b97-124">Dies ist **true** , wenn der-Modifizierer unterstützt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="d8b97-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="d8b97-125">Das "?" (der Benutzer wird aufgefordert, den Wähl Vorgang fortzusetzen) wird nie von einem liniengerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8b97-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="d8b97-126">Diese Flags ermöglichen es einer Anwendung, nach oben zu ermitteln, welche modifiziererer zur Generierung eines lineerr führen würden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="d8b97-127">Die Anwendung hat die Wahl, dass für nicht unterstützte Zeichen oder die "RAW"-Zeichenfolge aus [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) als Teil von Funktionen wie [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) oder [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial) vorab überprüft werden kann, und ermöglicht der Funktion, einen Fehler zu generieren, um zu erkennen, welcher nicht unterstützte Modifizierer zuerst in der Zeichenfolge auftritt.</span><span class="sxs-lookup"><span data-stu-id="d8b97-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**linedevcapflags \_ highlevcomp**</span><span class="sxs-lookup"><span data-stu-id="d8b97-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-129">Gibt an, ob in dieser Zeile allgemeine Kompatibilitäts Informationselemente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**linedevcapflags \_ lowlevcomp**</span><span class="sxs-lookup"><span data-stu-id="d8b97-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-131">Gibt an, ob Kompatibilitäts Informationselemente auf niedriger Ebene in dieser Zeile unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**linedevcapflags \_ MediaControl**</span><span class="sxs-lookup"><span data-stu-id="d8b97-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-133">Gibt an, ob Medien Steuerungs Vorgänge für Aufrufe in dieser Zeile verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d8b97-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**linedevcapflags- \_ MSP**</span><span class="sxs-lookup"><span data-stu-id="d8b97-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-135">Gibt an, ob der Zeile ein Medien Dienstanbieter (MSP) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8b97-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="d8b97-136">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="d8b97-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**linedevcapflags \_ multipleaddr**</span><span class="sxs-lookup"><span data-stu-id="d8b97-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-138">Gibt an, ob [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)oder [**TSPI \_ linedial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) mehrere Adressen gleichzeitig behandeln kann (wie bei umgekehrtem Multiplexing).</span><span class="sxs-lookup"><span data-stu-id="d8b97-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8b97-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**"linedevcapflags" \_ privateobjects**</span><span class="sxs-lookup"><span data-stu-id="d8b97-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8b97-140">Gibt an, ob [anbieterspezifische Schnittstellen](./provider-specific-interfaces.md) implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d8b97-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="d8b97-141">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="d8b97-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8b97-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8b97-142">Remarks</span></span>

<span data-ttu-id="d8b97-143">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="d8b97-143">No extensibility.</span></span> <span data-ttu-id="d8b97-144">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="d8b97-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b97-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8b97-145">Requirements</span></span>



| <span data-ttu-id="d8b97-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8b97-146">Requirement</span></span> | <span data-ttu-id="d8b97-147">Wert</span><span class="sxs-lookup"><span data-stu-id="d8b97-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d8b97-148">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d8b97-148">TAPI version</span></span><br/> | <span data-ttu-id="d8b97-149">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d8b97-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d8b97-150">Header</span><span class="sxs-lookup"><span data-stu-id="d8b97-150">Header</span></span><br/>       | <dl> <span data-ttu-id="d8b97-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b97-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b97-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8b97-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b97-153">**lineclose**</span><span class="sxs-lookup"><span data-stu-id="d8b97-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="d8b97-154">**linedial**</span><span class="sxs-lookup"><span data-stu-id="d8b97-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="d8b97-155">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="d8b97-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="d8b97-156">**linetranslateaddress**</span><span class="sxs-lookup"><span data-stu-id="d8b97-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

