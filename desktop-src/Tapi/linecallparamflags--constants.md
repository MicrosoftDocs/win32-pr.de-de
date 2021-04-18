---
description: Die linecallparamflags- \_ Konstanten beschreiben verschiedene Statusflags für einen-Befehl.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: LINECALLPARAMFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357533"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="068f3-103">Linecallparamflags- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="068f3-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="068f3-104">Die **linecallparamflags \_** -Konstanten beschreiben verschiedene Statusflags für einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="068f3-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="068f3-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**linecallparamflags- \_ blockid**</span><span class="sxs-lookup"><span data-stu-id="068f3-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-106">Die Absender Identität sollte verborgen sein (Block Aufrufer-ID).</span><span class="sxs-lookup"><span data-stu-id="068f3-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**linecallparamflags \_ destoffhook**</span><span class="sxs-lookup"><span data-stu-id="068f3-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-108">Das Telefon der angerufenen Partei sollte automatisch OFFHOOK werden.</span><span class="sxs-lookup"><span data-stu-id="068f3-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**linecallparamflags im \_ Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="068f3-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-110">Der-Befehl sollte aus einer Darstellung im Leerlauf Aussehen und nicht an einem in Bearbeitung befindlichen-Vorgang teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="068f3-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="068f3-111">Wenn bei Verwendung der [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) -Funktion der Wert für linecallparamflags \_ nicht festgelegt ist und ein vorhandener-Befehl in der Zeile vorhanden ist, unterbricht die Funktion ggf. den vorhandenen-Befehl, um den neuen-Befehl zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="068f3-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="068f3-112">Wenn kein vorhandener-Befehl vorhanden ist, wird der neue-Befehl von der-Funktion wie angegeben aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="068f3-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**linecallparamflags \_ noholdconference**</span><span class="sxs-lookup"><span data-stu-id="068f3-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-114">Dieses Bit wird nur in Verbindung mit [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) und [**lineprepareaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)verwendet.</span><span class="sxs-lookup"><span data-stu-id="068f3-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="068f3-115">Die Adresse, die mit dem aktuellen-Befehl übertragen werden soll, wird im **targetAddress** -Member in [**linecallparametriams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)angegeben.</span><span class="sxs-lookup"><span data-stu-id="068f3-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="068f3-116">Der-Beratungs Befehl zeichnet den Wählton nicht physisch vom Switch, sondern durch verschiedene aufrufseinstellerzustände (z. b. unter Wahl und Fortsetzung).</span><span class="sxs-lookup"><span data-stu-id="068f3-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="068f3-117">Wenn der Verbindungs Gespräch den Status "verbunden" erreicht, wird die Konferenz automatisch eingerichtet. der ursprüngliche-Befehl, der im verbundenen Zustand verbleibt, wechselt in den Status "übertragen". der Beratungs Rückruf wechselt in den Status "übertragen". der hconfcallenter wechselt in den Status "verbunden".</span><span class="sxs-lookup"><span data-stu-id="068f3-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="068f3-118">Wenn beim Rückruf ein Fehler auftritt (in den Zustand "getrennt", gefolgt von "inaktiv"), wechselt der "hconfcallcenter" auch in den Leerlauf Status, und der ursprüngliche-Befehl (der möglicherweise eine vorhandene Konferenz war, im Fall von " **lineprepareadddeconference**") verbleibt im verbundenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="068f3-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="068f3-119">Die ursprünglichen Parteien (oder Parteien) nehmen nie an, dass der-Befehl nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="068f3-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="068f3-120">Diese Funktion wird häufig verwendet, um einen Supervisor zu einem ACD-Agent-Aufruf hinzuzufügen, wenn dies notwendig ist, um Interaktionen mit einem unate-Aufrufer</span><span class="sxs-lookup"><span data-stu-id="068f3-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**linecallparamflags \_ onesteptransfer**</span><span class="sxs-lookup"><span data-stu-id="068f3-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-122">Dieses Bit wird nur in Verbindung mit [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)verwendet.</span><span class="sxs-lookup"><span data-stu-id="068f3-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="068f3-123">Er kombiniert den Vorgang von **lineSetupTransfer** , gefolgt von [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial) bei einem Rückruf in einem einzigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="068f3-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="068f3-124">Die Adresse, die gewählt werden soll, wird im **targetAddress** -Member in [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="068f3-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="068f3-125">Der ursprüngliche Aufruf wird in den *onholdpdingtransfer* -Status versetzt, als ob **lineSetupTransfer** normal aufgerufen wurde, und der Anruf wird normal eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="068f3-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="068f3-126">Die Anwendung muss weiterhin " [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) " aufruft, um die Übertragung zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="068f3-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="068f3-127">Diese Funktion wird häufig verwendet, wenn eine Übertragung von einem Server über einen Aufruf Steuerungs Link eines Drittanbieters aufgerufen wird, da solche Verknüpfungen häufig den normalen zweistufigen Prozess nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="068f3-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**linecallparamflags- \_ origoffhook**</span><span class="sxs-lookup"><span data-stu-id="068f3-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-129">Das Telefon des Absenders sollte automatisch OFFHOOK werden.</span><span class="sxs-lookup"><span data-stu-id="068f3-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**linecallparamflags \_ predictivedial**</span><span class="sxs-lookup"><span data-stu-id="068f3-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-131">Dieses Bit wird nur verwendet, wenn ein Aufruf für eine Adresse mit Predictive diwähl-Funktion erfolgt (lineaddrcapflags \_ predictivedialer ist im Member **dwaddrcapflags** in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="068f3-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="068f3-132">Das Bit muss aktiviert sein, um die erweiterten Aufrufe und/oder Geräte Überwachungsfunktionen des Geräts zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="068f3-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="068f3-133">Wenn dieses Bit nicht auf ON festgelegt ist, wird der Anruf ohne erweiterten Anrufstatus oder Medientyp Überwachung platziert, und es wird keine automatische Übertragung basierend auf dem Anrufstatus initiiert.</span><span class="sxs-lookup"><span data-stu-id="068f3-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="068f3-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**linecallparamflags- \_ sicher**</span><span class="sxs-lookup"><span data-stu-id="068f3-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="068f3-135">Der-Befehl sollte als sicher eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="068f3-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="068f3-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="068f3-136">Remarks</span></span>

<span data-ttu-id="068f3-137">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="068f3-137">No extensibility.</span></span> <span data-ttu-id="068f3-138">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="068f3-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="068f3-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="068f3-139">Requirements</span></span>



| <span data-ttu-id="068f3-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="068f3-140">Requirement</span></span> | <span data-ttu-id="068f3-141">Wert</span><span class="sxs-lookup"><span data-stu-id="068f3-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="068f3-142">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="068f3-142">TAPI version</span></span><br/> | <span data-ttu-id="068f3-143">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="068f3-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="068f3-144">Header</span><span class="sxs-lookup"><span data-stu-id="068f3-144">Header</span></span><br/>       | <dl> <span data-ttu-id="068f3-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="068f3-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068f3-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="068f3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068f3-147">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="068f3-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="068f3-148">**Linecallparametriams**</span><span class="sxs-lookup"><span data-stu-id="068f3-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="068f3-149">**linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="068f3-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="068f3-150">**linedial**</span><span class="sxs-lookup"><span data-stu-id="068f3-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="068f3-151">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="068f3-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="068f3-152">**lineprepareaddumconference**</span><span class="sxs-lookup"><span data-stu-id="068f3-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="068f3-153">**linesetupconference**</span><span class="sxs-lookup"><span data-stu-id="068f3-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="068f3-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="068f3-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




