---
description: Die managechannel-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), der logische Kanäle öffnet und schließt.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816:: managechannel-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042066"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="15e1a-103">ISCardISO7816:: managechannel-Methode</span><span class="sxs-lookup"><span data-stu-id="15e1a-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="15e1a-104">\[Die **managechannel** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="15e1a-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="15e1a-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15e1a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15e1a-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="15e1a-107">Die **managechannel** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der logische Kanäle öffnet und schließt.</span><span class="sxs-lookup"><span data-stu-id="15e1a-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="15e1a-108">Die Open-Funktion öffnet einen neuen logischen Channel, der nicht der grundlegende ist.</span><span class="sxs-lookup"><span data-stu-id="15e1a-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="15e1a-109">Optionen werden für die Karte bereitgestellt, um eine logische Channelnummer zuzuweisen, oder, wenn die Nummer des logischen Kanals an die Karte übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="15e1a-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="15e1a-110">Die Close-Funktion schließt explizit einen logischen Channel, der nicht der grundlegende ist.</span><span class="sxs-lookup"><span data-stu-id="15e1a-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="15e1a-111">Nach dem erfolgreichen Abschluss des Vorgangs sollte der logische Kanal zur erneuten Verwendung verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="15e1a-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e1a-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="15e1a-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="15e1a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="15e1a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15e1a-114">*bychannelstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e1a-115">Die Bit-B8 von P1 wird verwendet, um die Open-Funktion oder die Close-Funktion anzugeben. Wenn die "B8" den Wert "0" hat, öffnet "Channel verwalten" einen logischen Kanal</span><span class="sxs-lookup"><span data-stu-id="15e1a-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="15e1a-116">P1 = ' 00 ' zum Öffnen</span><span class="sxs-lookup"><span data-stu-id="15e1a-116">P1 = '00' to open</span></span>

<span data-ttu-id="15e1a-117">P1 = ' 80 ' zum Schließen</span><span class="sxs-lookup"><span data-stu-id="15e1a-117">P1 = '80' to close</span></span>

<span data-ttu-id="15e1a-118">Weitere Werte sind RFU.</span><span class="sxs-lookup"><span data-stu-id="15e1a-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="15e1a-119">*bychannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e1a-120">Für die Open-Funktion (P1 = ' 00 ') werden die Bits B1 und B2 von P2 verwendet, um die logische Channelnummer auf die gleiche Weise wie im-Klassen-Byte zu codieren, die anderen Bits von P2 sind RFU.</span><span class="sxs-lookup"><span data-stu-id="15e1a-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="15e1a-121">Wenn B1 und B2 von P2 **null** sind, weist die Karte eine logische Channelnummer zu, die in Bits B1 und B2 des Datenfelds zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="15e1a-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="15e1a-122">Wenn B1 und/oder B2 von P2 nicht **null** sind, codieren Sie eine andere logische Kanalnummer als die Basis. dann öffnet die Karte die extern zugewiesene logische Kanalnummer.</span><span class="sxs-lookup"><span data-stu-id="15e1a-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="15e1a-123">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15e1a-124">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="15e1a-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="15e1a-125">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="15e1a-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="15e1a-126">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15e1a-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15e1a-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15e1a-127">Return value</span></span>

<span data-ttu-id="15e1a-128">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="15e1a-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="15e1a-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="15e1a-129">Return code</span></span>                                                                                   | <span data-ttu-id="15e1a-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15e1a-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="15e1a-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="15e1a-132">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="15e1a-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="15e1a-133"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="15e1a-134">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="15e1a-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="15e1a-135"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="15e1a-136">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="15e1a-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="15e1a-137"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="15e1a-138">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="15e1a-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="15e1a-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15e1a-139">Remarks</span></span>

<span data-ttu-id="15e1a-140">Wenn die Open-Funktion erfolgreich vom logischen Standard Kanal ausgeführt wird, muss der MF implizit als aktuelle DF ausgewählt werden, und der Sicherheitsstatus des neuen logischen Kanals sollte mit dem logischen Standard Kanal nach ATR übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="15e1a-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="15e1a-141">Der Sicherheitsstatus des neuen logischen Kanals sollte von dem eines beliebigen anderen logischen Kanals getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="15e1a-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="15e1a-142">Wenn die Open-Funktion erfolgreich von einem logischen Kanal ausgeführt wird, der nicht der Basis ist, wird die aktuelle DF des logischen Kanals, der den Befehl ausgegeben hat, als aktuelle DF ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="15e1a-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="15e1a-143">Außerdem sollte der Sicherheitsstatus für den neuen logischen Kanal mit dem Sicherheitsstatus des logischen Kanals identisch sein, von dem die Open-Funktion ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="15e1a-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="15e1a-144">Nach einer erfolgreichen Schließfunktion geht der Sicherheitsstatus, der sich auf diesen logischen Kanal bezieht, verloren.</span><span class="sxs-lookup"><span data-stu-id="15e1a-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="15e1a-145">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="15e1a-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="15e1a-146">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="15e1a-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="15e1a-147">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="15e1a-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15e1a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15e1a-148">Requirements</span></span>



| <span data-ttu-id="15e1a-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15e1a-149">Requirement</span></span> | <span data-ttu-id="15e1a-150">Wert</span><span class="sxs-lookup"><span data-stu-id="15e1a-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15e1a-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15e1a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="15e1a-152">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="15e1a-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15e1a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="15e1a-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15e1a-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15e1a-155">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="15e1a-155">End of client support</span></span><br/>    | <span data-ttu-id="15e1a-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="15e1a-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="15e1a-157">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="15e1a-157">End of server support</span></span><br/>    | <span data-ttu-id="15e1a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15e1a-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="15e1a-159">Header</span><span class="sxs-lookup"><span data-stu-id="15e1a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e1a-160"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15e1a-161">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="15e1a-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="15e1a-162"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15e1a-163">DLL</span><span class="sxs-lookup"><span data-stu-id="15e1a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e1a-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e1a-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15e1a-165">IID</span><span class="sxs-lookup"><span data-stu-id="15e1a-165">IID</span></span><br/>                      | <span data-ttu-id="15e1a-166">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="15e1a-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="15e1a-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15e1a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e1a-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="15e1a-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
