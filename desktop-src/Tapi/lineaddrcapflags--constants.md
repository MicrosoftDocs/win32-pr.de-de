---
description: Die \_ Bit-Flag-Konstanten von lineaddrcapflags werden im dwaddrcapflags-Member der lineaddresscaps-Datenstruktur verwendet, um verschiedene boolesche Adress Funktionen zu beschreiben.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: LINEADDRCAPFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369474"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="b6032-103">Lineaddrcapflags- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="b6032-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="b6032-104">Die Bit-Flag-Konstanten von **lineaddrcapflags** \_ werden im **dwaddrcapflags** -Member der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Datenstruktur verwendet, um verschiedene boolesche Adress Funktionen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b6032-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="b6032-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**lineaddrcapflags " \_ akzepttoalert"**</span><span class="sxs-lookup"><span data-stu-id="b6032-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-106">**True** , wenn ein Angebots Befehl mithilfe von [**lineaccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) akzeptiert werden muss, um zu beginnen, die Benutzer an beiden Enden des Aufrufens zu warnen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="b6032-107">Dies wird in der Regel nur mit ISDN verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6032-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**lineaddrcapflags- \_ acdgroup**</span><span class="sxs-lookup"><span data-stu-id="b6032-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-109">Die Adresse unterstützt [ACD-Gruppen](about-call-center-controls.md#acd-group-object) in Verbindung mit callcentervorgängen.</span><span class="sxs-lookup"><span data-stu-id="b6032-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="b6032-110">Weitere Informationen zu ACD-Gruppen finden Sie unter Informationen [zu Callcenter](./about-call-center-controls.md) -Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="b6032-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**lineaddrcapflags \_ autoReconnect**</span><span class="sxs-lookup"><span data-stu-id="b6032-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-112">Gibt an, ob durch das Löschen eines Beratungs Aufrufes bei der Beratungs Aufbewahrung automatisch erneut eine Verbindung mit dem Rückruf</span><span class="sxs-lookup"><span data-stu-id="b6032-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="b6032-113">**True** , wenn die erneute Verbindungs Herstellung automatisch erfolgt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**lineaddrcapflags \_ blockiddefault**</span><span class="sxs-lookup"><span data-stu-id="b6032-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-115">Gibt an, ob das Netzwerk bei einem Aufruf für diese Adresse standardmäßig Aufrufer-ID-Informationen sendet oder blockiert.</span><span class="sxs-lookup"><span data-stu-id="b6032-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="b6032-116">**True** gibt an, dass die Bezeichnerinformationen standardmäßig blockiert werden. bei " **false**" werden standardmäßig die Bezeichnerinformationen übertragen.</span><span class="sxs-lookup"><span data-stu-id="b6032-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**lineaddrcapflags \_ blockidoverride**</span><span class="sxs-lookup"><span data-stu-id="b6032-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-118">Gibt an, ob die Standardeinstellung für das Senden oder Blockieren von Aufrufer-ID-Informationen pro Aufruf überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="b6032-119">**True** gibt an, dass außer Kraft Setzung möglich ist. **false** gibt an, dass außer Kraft Setzung nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="b6032-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**completionid für lineaddrcapflags \_**</span><span class="sxs-lookup"><span data-stu-id="b6032-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-121">Gibt an, ob die von [**linecompletecallzurück**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) gegebenen Vervollständigungs-IDs nützlich und eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="b6032-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="b6032-122">**True** , wenn nützlich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**"lineaddrcapflags" ( \_ confdrop)**</span><span class="sxs-lookup"><span data-stu-id="b6032-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-124">" **True** ", wenn " [**linedrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) " bei einem übergeordneten Konferenzgespräch auch den Nebeneffekt hat, dass die anderen Parteien, die am Konferenzgespräch beteiligt sind, gelöscht werden sollen. " **False** ", wenn durch das Löschen eines Konferenz Aufrufes den anderen Parteien weiterhin untereinander gesprochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**lineaddrcapflags- \_ conferenceheld**</span><span class="sxs-lookup"><span data-stu-id="b6032-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-126">Gibt an, ob ein hart gehaltene-Befehl an die übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="b6032-127">Häufig können nur Aufrufe der Beratungs Aufbewahrung als Konferenz Aufruf hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b6032-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**lineaddrcapflags- \_ conferencemake**</span><span class="sxs-lookup"><span data-stu-id="b6032-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-129">Gibt an, ob ein vollständig neuer-Rückruf für die Verwendung als Rückruf (zum Hinzufügen) auf der Konferenz erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**lineaddrcapflags \_ destoffhook**</span><span class="sxs-lookup"><span data-stu-id="b6032-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-131">Gibt an, ob das Telefon der angerufenen Partei beim Ausführen von Aufrufen automatisch erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**lineaddrcapflags \_ gewählt**</span><span class="sxs-lookup"><span data-stu-id="b6032-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-133">Gibt an, ob eine Zieladresse für diese Adresse für einen-Rückruf gewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="b6032-134">**True** , wenn eine Zieladresse gewählt werden muss. **False** , wenn die Zieladresse (wie bei einem "heißen Telefon") korrigiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6032-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**lineaddrcapflags ( \_ f)**</span><span class="sxs-lookup"><span data-stu-id="b6032-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-136">Gibt an, ob die Anrufweiterleitung für ausgelastet und für keine Antwort unterschiedliche Weiterleitungs Adressen verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="b6032-137">Dieses Flag ist nur dann von Bedeutung, wenn die Weiterleitung für ausgelastet und keine Antwort separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="b6032-138">Dieses Flag ist **true** , wenn die Weiterleitung für ausgelastet und keine Antwort unterschiedliche Zieladressen verwenden kann. Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**lineaddrcapflags ( \_ f)**</span><span class="sxs-lookup"><span data-stu-id="b6032-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-140">Gibt an, ob die aufrufweiterleitung die Einrichtung eines Beratungs Aufrufens einschließt.</span><span class="sxs-lookup"><span data-stu-id="b6032-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**lineaddrcapflags, \_ f.**</span><span class="sxs-lookup"><span data-stu-id="b6032-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-142">Gibt an, ob interne und externe Aufrufe an verschiedene Weiterleitungs Adressen weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b6032-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="b6032-143">Dieses Flag ist nur sinnvoll, wenn die Weiterleitung interner und externer Aufrufe separat gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="b6032-144">Dieses Flag ist **true** , wenn interne und externe Aufrufe an verschiedene Zieladressen weitergeleitet werden können. Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**lineaddrcapflags-" \_ f"**</span><span class="sxs-lookup"><span data-stu-id="b6032-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-146">Gibt an, ob die Anzahl der Ringe für eine Antwort ohne Antwort angegeben werden kann, wenn Aufrufe ohne Antwort weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b6032-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="b6032-147">Wenn der Wert **true** ist, wird der gültige Bereich in den Elementen **dwminfwdnumrings** und **dwmaxfwdnumrings** der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b6032-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**lineaddrcapflags \_ fwdstatus valid**</span><span class="sxs-lookup"><span data-stu-id="b6032-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-149">Gibt an, ob der Weiterleitungs Status in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur für diese Adresse gültig ist oder höchstens eine "beste Schätzung" ist, weil keine genaue Bestätigung durch den Switch oder das Netzwerk vorliegt.</span><span class="sxs-lookup"><span data-stu-id="b6032-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**lineaddrcapflags \_ holdmakesnew**</span><span class="sxs-lookup"><span data-stu-id="b6032-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-151">Wenn ein Anruf für diese Adresse angehalten wird (mit [**linehold**](/windows/desktop/api/Tapi/nf-tapi-linehold) oder externer Aktion), wird automatisch ein neuer Anruf erstellt (höchstwahrscheinlich in linecallstate \_ Dialtone).</span><span class="sxs-lookup"><span data-stu-id="b6032-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**lineaddrcapflags \_ noexternalcalls**</span><span class="sxs-lookup"><span data-stu-id="b6032-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-153">Die Adresse ist einer internen Zeile in einer PBX zugeordnet, die so eingeschränkt ist, dass Sie nicht zum Platzieren von Anrufen an eine Adresse außerhalb des Schalters verwendet werden kann (z. b. eine Gegenseite).</span><span class="sxs-lookup"><span data-stu-id="b6032-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="b6032-154">Die Anwendung kann diese Angabe verwenden, um dem Benutzer zu helfen, die richtige aufrufdarstellung auszuwählen, die zum Ausführen eines Aufrufens verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6032-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="b6032-155">Wenn dieses Bit deaktiviert ist, gibt es nicht notwendigerweise an, dass die Adresse zum Ausführen externer Aufrufe verwendet werden kann, da der Dienstanbieter möglicherweise nicht der Typ der Zeile ist.</span><span class="sxs-lookup"><span data-stu-id="b6032-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**lineaddrcapflags \_ nointernalcalls**</span><span class="sxs-lookup"><span data-stu-id="b6032-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-157">Die Adresse ist einer direkten Co-Linie (trunk) zugeordnet und kann nicht verwendet werden, um interne Aufrufe an eine PBX durchführen.</span><span class="sxs-lookup"><span data-stu-id="b6032-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="b6032-158">Die Anwendung kann diese Angabe verwenden, um dem Benutzer zu helfen, die richtige aufrufdarstellung auszuwählen, die zum Ausführen eines Aufrufens verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6032-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="b6032-159">Wenn dieses Bit deaktiviert ist, gibt es nicht notwendigerweise an, dass die Adresse verwendet werden kann, um interne Aufrufe durchzuführen, da der Dienstanbieter möglicherweise nicht dem Zeittyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="b6032-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**lineaddrcapflags \_ nopstnadresssstranslations**</span><span class="sxs-lookup"><span data-stu-id="b6032-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-161">Diese Adresse unterstützt keine Übersetzung der öffentlichen, übersetzte Telefon Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="b6032-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="b6032-162">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="b6032-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**lineaddrcapflags \_ origoffhook**</span><span class="sxs-lookup"><span data-stu-id="b6032-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-164">Gibt an, ob das Telefon der Ursprungs Partei beim Ausführen von Aufrufen automatisch als OFFHOOK verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**lineaddrcapflags- \_ partialdial**</span><span class="sxs-lookup"><span data-stu-id="b6032-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-166">Gibt an, ob partielle Wählbarkeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6032-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**lineaddrcapflags \_ pickupcallwait**</span><span class="sxs-lookup"><span data-stu-id="b6032-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-168">" **True** ", wenn " [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) " verwendet werden kann, um einen vom Benutzer erkannten Befehl als Aufrufe aufzurufen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b6032-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**lineaddrcapflags \_ pickupgroupid**</span><span class="sxs-lookup"><span data-stu-id="b6032-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-170">Gibt an, ob eine Gruppen-ID für die aufrufabholung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b6032-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**lineaddrcapflags \_ predictivedialer**</span><span class="sxs-lookup"><span data-stu-id="b6032-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-172">Diese Adresse verfügt über erweiterte Überwachungsfunktionen zum Aufrufen des Status, die auf ausgehende Aufrufe angewendet werden können, um Aufruf Zustände, wie z. b. " *geben*", " *ausgelastet*", " *specialinfo*" und " *verbunden*", oder den Medientyp des Geräts zu bestimmen</span><span class="sxs-lookup"><span data-stu-id="b6032-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="b6032-173">Sie kann auch die Möglichkeit haben, ausgehende Aufrufe automatisch an eine andere Adresse zu übertragen, wenn ein Aufruf einen vordefinierten Satz von Zuständen erreicht.</span><span class="sxs-lookup"><span data-stu-id="b6032-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**lineaddrcapflags- \_ Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="b6032-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-175">Diese Adresse ist nicht mit einer bestimmten Station oder einem physischen Gerät verknüpft, sondern ist eine Position, an der Anrufe auf eine weitere Verarbeitung warten.</span><span class="sxs-lookup"><span data-stu-id="b6032-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="b6032-176">Die in der Warteschlange platzierten Aufrufe können eine bestimmte Behandlung erhalten.</span><span class="sxs-lookup"><span data-stu-id="b6032-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="b6032-177">Sie können auch automatisch übertragen werden, wenn eine bestimmte Ressource verfügbar wird (z. b. wenn es sich bei der Warteschlange um eine ACD-Warteschlange handelt und Aufrufe auf einen verfügbaren Agent warten).</span><span class="sxs-lookup"><span data-stu-id="b6032-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**lineaddrcapflags- \_ Routepoint**</span><span class="sxs-lookup"><span data-stu-id="b6032-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-179">Diese Adresse ist nicht mit einer bestimmten Station oder einem physischen Gerät verknüpft, sondern ist eine Anlaufstelle, an der Anrufe auf das Routing durch die Anwendung warten (die Anwendung überprüft die aufgerufene Adresse und kann den Aufruf an eine andere Adresse umleiten).</span><span class="sxs-lookup"><span data-stu-id="b6032-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="b6032-180">Der-Befehl kann auch automatisch übertragen werden, wenn ein Routing Timeout abläuft (der Switch nimmt normalerweise ein Standard Routing an).</span><span class="sxs-lookup"><span data-stu-id="b6032-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**lineaddrcapflags \_ sicher**</span><span class="sxs-lookup"><span data-stu-id="b6032-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-182">Gibt an, ob Aufrufe für diese Adresse zum Zeitpunkt des Aufrufs der Einrichtung sicher gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="b6032-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**lineaddrcapflags \_ setcallingid**</span><span class="sxs-lookup"><span data-stu-id="b6032-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-184">Die Anwendung kann festlegen, dass das **callingpartyid** -Element beim Aufrufen von [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) und anderen Funktionen, die eine **linecallparameterstruktur** akzeptieren, in [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) Metern festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b6032-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="b6032-185">Wenn der Inhalt des Bezeichners akzeptabel und ein Pfad verfügbar ist, übergibt der Dienstanbieter den Bezeichner an die aufgerufene Partei, um die Identität der aufrufenden Partei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6032-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**lineaddrcapflags \_ setupconfnull**</span><span class="sxs-lookup"><span data-stu-id="b6032-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-187">Gibt an, ob das Einrichten eines Konferenz Aufrufes mit einem ersten-Befehl (**false**) oder ohne ersten-Rückruf (**true**) beginnt.</span><span class="sxs-lookup"><span data-stu-id="b6032-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**lineaddrcapflags \_ transferlake**</span><span class="sxs-lookup"><span data-stu-id="b6032-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-189">Gibt an, ob ein hart gehaltene-Rückruf übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6032-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="b6032-190">Häufig können nur Aufrufe der Beratungs Aufbewahrung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b6032-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6032-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**lineaddrcapflags \_ transfermake**</span><span class="sxs-lookup"><span data-stu-id="b6032-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6032-192">Gibt an, ob ein vollständig neuer-aufrufbedarf zur Verwendung als bei der Übertragung verwendetes Gespräch eingerichtet werden kann</span><span class="sxs-lookup"><span data-stu-id="b6032-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6032-193">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6032-193">Remarks</span></span>

<span data-ttu-id="b6032-194">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="b6032-194">No extensibility.</span></span> <span data-ttu-id="b6032-195">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="b6032-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6032-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6032-196">Requirements</span></span>



| <span data-ttu-id="b6032-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6032-197">Requirement</span></span> | <span data-ttu-id="b6032-198">Wert</span><span class="sxs-lookup"><span data-stu-id="b6032-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6032-199">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b6032-199">TAPI version</span></span><br/> | <span data-ttu-id="b6032-200">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b6032-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b6032-201">Header</span><span class="sxs-lookup"><span data-stu-id="b6032-201">Header</span></span><br/>       | <dl> <span data-ttu-id="b6032-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6032-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6032-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6032-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6032-204">**lineaccept**</span><span class="sxs-lookup"><span data-stu-id="b6032-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="b6032-205">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="b6032-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="b6032-206">**Lineaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="b6032-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="b6032-207">**Linecallparametriams**</span><span class="sxs-lookup"><span data-stu-id="b6032-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="b6032-208">**linecompletecall**</span><span class="sxs-lookup"><span data-stu-id="b6032-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="b6032-209">**linedrop**</span><span class="sxs-lookup"><span data-stu-id="b6032-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="b6032-210">**linehold**</span><span class="sxs-lookup"><span data-stu-id="b6032-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="b6032-211">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="b6032-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="b6032-212">**linepickup**</span><span class="sxs-lookup"><span data-stu-id="b6032-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

