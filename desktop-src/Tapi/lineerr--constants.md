---
description: Im folgenden finden Sie eine Liste von Fehlercodes, die TAPI zurückgeben kann, wenn Vorgänge für Zeilen, Adressen oder Aufrufe aufgerufen werden.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: LINEERR_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369292"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="88173-103">Lineerr- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="88173-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="88173-104">Im folgenden finden Sie eine Liste von Fehlercodes, die TAPI zurückgeben kann, wenn Vorgänge für Zeilen, Adressen oder Aufrufe aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="88173-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="88173-105">Weitere Informationen zum Bestimmen der Fehlercodes, die eine bestimmte Funktion zurückgeben kann, finden Sie in den Beschreibungen zu den einzelnen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="88173-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="88173-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**lineerr \_ adressiblockiert**</span><span class="sxs-lookup"><span data-stu-id="88173-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-107">Die angegebene Adresse wird für den angegebenen-Befehl nicht gewählt.</span><span class="sxs-lookup"><span data-stu-id="88173-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**lineerr \_ adressiblockiert**</span><span class="sxs-lookup"><span data-stu-id="88173-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-109">Für die Ziel-Telefon Adresse ist die aktivierte Sperre aktiviert.</span><span class="sxs-lookup"><span data-stu-id="88173-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**lineerr \_ zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="88173-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-111">Die Zeile kann aufgrund einer permanenten Bedingung nicht geöffnet werden, z. b. bei einem seriellen Anschluss, der exklusiv von einem anderen Prozess geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="88173-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**lineerr \_ badde viceid**</span><span class="sxs-lookup"><span data-stu-id="88173-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-113">Der angegebene Geräte Bezeichner oder zeilige Geräte Bezeichner, z. b. in einem *dwenviceid* -Parameter, ist ungültig oder liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="88173-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**lineerr \_ bearermodeunnütz**</span><span class="sxs-lookup"><span data-stu-id="88173-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-115">Der bearermodusmember in [**linecallparameams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) ist ungültig, der in **linecallparameams** angegebene bearermodus ist nicht verfügbar, oder der callbearermodus kann nicht in den angegebenen bearermodus geändert werden.</span><span class="sxs-lookup"><span data-stu-id="88173-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**lineerr \_ billingreworfene**</span><span class="sxs-lookup"><span data-stu-id="88173-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-117">Der Abrechnungsmodus des Aufrufes wurde zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="88173-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**lineerr \_ callunnütz**</span><span class="sxs-lookup"><span data-stu-id="88173-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-119">Alle Aufrufe für die angegebene Adresse werden zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="88173-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**"lineerr \_ completionüberlauf"**</span><span class="sxs-lookup"><span data-stu-id="88173-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-121">Die maximal zulässige Anzahl von ausstehenden Aufstellungen wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="88173-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**lineerr- \_ Konferenz Name**</span><span class="sxs-lookup"><span data-stu-id="88173-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-123">Die maximale Anzahl von Parteien für eine Konferenz wurde erreicht, oder die angeforderte Anzahl von Parteien kann nicht erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="88173-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**lineerr- \_ dialabrechnung**</span><span class="sxs-lookup"><span data-stu-id="88173-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-125">Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**lineerr- \_ dialdialtone**</span><span class="sxs-lookup"><span data-stu-id="88173-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-127">Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**lineerr- \_ dialprompt**</span><span class="sxs-lookup"><span data-stu-id="88173-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-129">Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**lineerr- \_ dialquiet**</span><span class="sxs-lookup"><span data-stu-id="88173-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-131">Der Parameter für die dialable-Adresse enthält Wähl Bare Steuerzeichen, die nicht vom Dienstanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**lineerr- \_ dialvoicedetect**</span><span class="sxs-lookup"><span data-stu-id="88173-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-133">Verwendung des wählmodifizierers (:) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88173-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="88173-134">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**lineerr \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="88173-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-136">Der-Rückruf wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="88173-136">The call has been disconnected.</span></span> <span data-ttu-id="88173-137">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**lineerr \_ incompatibleapiversion**</span><span class="sxs-lookup"><span data-stu-id="88173-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-139">Die Anwendung hat eine TAPI-Version oder einen Versions Bereich angefordert, der entweder mit der telefonieimplementierung der Telefonie-API und dem entsprechenden Dienstanbieter kompatibel ist oder nicht von dieser unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="88173-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**lineerr \_ incompatibleextversion**</span><span class="sxs-lookup"><span data-stu-id="88173-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-141">Die Anwendung hat einen Erweiterungs Versions Bereich angefordert, der entweder ungültig ist oder vom entsprechenden Dienstanbieter nicht unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="88173-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**lineerr \_ inifilebeschädigt**</span><span class="sxs-lookup"><span data-stu-id="88173-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-143">Die Telephon.ini Datei kann aufgrund interner Inkonsistenzen oder Formatierungs Probleme nicht ordnungsgemäß von TAPI gelesen oder verstanden werden.</span><span class="sxs-lookup"><span data-stu-id="88173-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="88173-144">Beispielsweise kann der \[ Abschnitt "Standorte" \] , "Karten" oder " \[ Länder" \] \[ \] der Telephon.ini Datei beschädigt oder inkonsistent sein.</span><span class="sxs-lookup"><span data-stu-id="88173-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**lineerr- \_ InUse**</span><span class="sxs-lookup"><span data-stu-id="88173-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-146">Das liniengerät wird derzeit verwendet und kann derzeit nicht konfiguriert werden, die Hinzufügung einer Partei, das zulassen eines Aufrufes zulassen, das Platzieren eines Aufrufes zulassen oder das übertragen eines Aufrufes erlauben.</span><span class="sxs-lookup"><span data-stu-id="88173-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**lineerr- \_ invaladdress**</span><span class="sxs-lookup"><span data-stu-id="88173-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-148">Eine angegebene Adresse ist entweder ungültig oder nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="88173-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="88173-149">Wenn der Wert ungültig ist, enthält die Adresse ungültige Zeichen oder Ziffern, oder die Zieladresse enthält Wähl Kontrollzeichen (W, @, $ oder?), die vom Dienstanbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="88173-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="88173-150">Wenn dies nicht zulässig ist, wird die angegebene Adresse entweder nicht der angegebenen Zeile zugewiesen oder ist für die Adressumleitung ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**lineerr \_ invaladressssid**</span><span class="sxs-lookup"><span data-stu-id="88173-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-152">Der angegebene Adress Bezeichner ist entweder ungültig oder liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="88173-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**lineerr \_ invaladdressmode**</span><span class="sxs-lookup"><span data-stu-id="88173-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-154">Der angegebene Adress Modus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**lineerr \_ invaladdressstate**</span><span class="sxs-lookup"><span data-stu-id="88173-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-156">Der angegebene Adress Zustand enthält mindestens ein Bit, das keine [**lineaddressstate- \_ Konstanten**](lineaddressstate--constants.md)ist.</span><span class="sxs-lookup"><span data-stu-id="88173-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**lineerr \_ invaladresssstype**</span><span class="sxs-lookup"><span data-stu-id="88173-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-158">Die Anwendung hat auf einen ungültigen adrestyp verwiesen.</span><span class="sxs-lookup"><span data-stu-id="88173-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="88173-159">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**lineerr \_ invalagentactivity**</span><span class="sxs-lookup"><span data-stu-id="88173-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-161">Die angegebene Agentaktivität ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**lineerr \_ invalagentactivity**</span><span class="sxs-lookup"><span data-stu-id="88173-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-163">Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe.</span><span class="sxs-lookup"><span data-stu-id="88173-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="88173-164">Das heißt, TAPI hat festgestellt, dass die aufrufenden Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="88173-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="88173-165">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**lineerr \_ invalagentgroup**</span><span class="sxs-lookup"><span data-stu-id="88173-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-167">Die angegebenen agentgruppeninformationen sind ungültig oder enthalten Fehler.</span><span class="sxs-lookup"><span data-stu-id="88173-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="88173-168">Die angeforderte Aktion wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88173-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**lineerr \_ invalagentgroup**</span><span class="sxs-lookup"><span data-stu-id="88173-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-170">Die Anwendung hat auf eine ungültige Agent-Gruppe verwiesen.</span><span class="sxs-lookup"><span data-stu-id="88173-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="88173-171">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**lineerr \_ invalagentid**</span><span class="sxs-lookup"><span data-stu-id="88173-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-173">Der angegebene Agent-Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**lineerr \_ invalagentid**</span><span class="sxs-lookup"><span data-stu-id="88173-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-175">Es wurde ein ungültiger Agent-Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="88173-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="88173-176">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**lineerr \_ invalagentsessionstate**</span><span class="sxs-lookup"><span data-stu-id="88173-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-178">Der agentsitzungsstatus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-178">The agent session state is invalid.</span></span> <span data-ttu-id="88173-179">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**lineerr \_ invalagentstate**</span><span class="sxs-lookup"><span data-stu-id="88173-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-181">Der angegebene Agentstatus ist ungültig oder enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="88173-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="88173-182">Es wurden keine Änderungen am Agentstatus der angegebenen Adresse vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="88173-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**lineerr \_ invalagentstate**</span><span class="sxs-lookup"><span data-stu-id="88173-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-184">Die Anwendung hat auf einen ungültigen Agent-Status verwiesen.</span><span class="sxs-lookup"><span data-stu-id="88173-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="88173-185">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**lineerr \_ invalapphandle**</span><span class="sxs-lookup"><span data-stu-id="88173-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-187">Das Anwendungs handle (z. b. durch einen *hlineapp* -Parameter angegeben) oder das Anwendungs Registrierungs Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**lineerr \_ invalappname**</span><span class="sxs-lookup"><span data-stu-id="88173-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-189">Der angegebene Anwendungsname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-189">The specified application name is invalid.</span></span> <span data-ttu-id="88173-190">Wenn ein Anwendungsname von der Anwendung angegeben wird, wird davon ausgegangen, dass die Zeichenfolge keine nicht anzeigbaren Zeichen enthält und mit 0 (null) beendet wird.</span><span class="sxs-lookup"><span data-stu-id="88173-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**lineerr \_ invalbearermode**</span><span class="sxs-lookup"><span data-stu-id="88173-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-192">Der angegebene bearermodus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**lineerr \_ invalcallcomplmode**</span><span class="sxs-lookup"><span data-stu-id="88173-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-194">Der angegebene Abschluss ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**lineerr \_ invalcallhandle**</span><span class="sxs-lookup"><span data-stu-id="88173-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-196">Das angegebene-Rückruf Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-196">The specified call handle is not valid.</span></span> <span data-ttu-id="88173-197">Beispielsweise ist das Handle nicht **null** , gehört jedoch nicht zur angegebenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="88173-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="88173-198">In einigen Fällen ist das angegebene Handle-Geräte Handle ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**lineerr \_ invalcallparametriams**</span><span class="sxs-lookup"><span data-stu-id="88173-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-200">Die angegebenen Parameter für den Rückruf sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**lineerr \_ invalcallprivilege**</span><span class="sxs-lookup"><span data-stu-id="88173-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-202">Der angegebene Parameter zum Aufrufen von Berechtigungen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**lineerr \_ invalcallselect**</span><span class="sxs-lookup"><span data-stu-id="88173-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-204">Der angegebene Select-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**lineerr \_ invalcallstate**</span><span class="sxs-lookup"><span data-stu-id="88173-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-206">Der aktuelle Zustand eines Aufrufens befindet sich nicht in einem gültigen Zustand für den angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="88173-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**lineerr \_ invalcallstatuelist**</span><span class="sxs-lookup"><span data-stu-id="88173-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-208">Die angegebene aufrufstatusliste ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**lineerr- \_ invalcard**</span><span class="sxs-lookup"><span data-stu-id="88173-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-210">Der in *dwcard* angegebene permanente Karten Bezeichner konnte in keinem Eintrag im \[ Karten Abschnitt der Registrierung gefunden werden \] .</span><span class="sxs-lookup"><span data-stu-id="88173-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**lineerr \_ invalcompletionid**</span><span class="sxs-lookup"><span data-stu-id="88173-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-212">Der Vervollständigungs Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**lineerr \_ invalconfcallhandle**</span><span class="sxs-lookup"><span data-stu-id="88173-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-214">Das angegebene Telefon Handle für den Konferenz Aufrufwert ist ungültig oder kein Handle für einen Konferenz Befehl.</span><span class="sxs-lookup"><span data-stu-id="88173-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**lineerr \_ invalberattcallhandle**</span><span class="sxs-lookup"><span data-stu-id="88173-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-216">Das angegebene Handle für den Beratungs Rückruf ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**lineerr \_ invalcountrycode**</span><span class="sxs-lookup"><span data-stu-id="88173-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-218">Der angegebene Code für Land oder Region ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**lineerr \_ invalentviceclass**</span><span class="sxs-lookup"><span data-stu-id="88173-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-220">Das liniengerät weist kein zugeordnetes Gerät für die angegebene Geräteklasse auf, oder die angegebene Zeile unterstützt die angegebene Geräteklasse nicht.</span><span class="sxs-lookup"><span data-stu-id="88173-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**lineerr \_ invaldebug-andle**</span><span class="sxs-lookup"><span data-stu-id="88173-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-222">Das Zeilen Geräte Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**lineerr \_ invaldialparametriams**</span><span class="sxs-lookup"><span data-stu-id="88173-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-224">Die Wähl Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**lineerr \_ invaldigitlist**</span><span class="sxs-lookup"><span data-stu-id="88173-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-226">Die angegebene Ziffern Liste ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**lineerr \_ invaldigitmode**</span><span class="sxs-lookup"><span data-stu-id="88173-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-228">Der angegebene Ziffern Modus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**lineerr- \_ invaldigits**</span><span class="sxs-lookup"><span data-stu-id="88173-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-230">Die angegebenen Beendigungs Ziffern sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**lineerr \_ invalextversion**</span><span class="sxs-lookup"><span data-stu-id="88173-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-232">Die Versionsnummer der Dienstanbieter Erweiterung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**lineerr- \_ invalfeature**</span><span class="sxs-lookup"><span data-stu-id="88173-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-234">Der *dwfeature* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**lineerr- \_ invalfeature**</span><span class="sxs-lookup"><span data-stu-id="88173-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-236">Die Anwendung hat eine Funktion aufgerufen, die in dieser Zeile nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="88173-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**lineerr \_ invalgroupid**</span><span class="sxs-lookup"><span data-stu-id="88173-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-238">Der angegebene Gruppen Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**lineerr- \_ invallinehandle**</span><span class="sxs-lookup"><span data-stu-id="88173-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-240">Der angegebene Rückruf, das Gerät, das Zeilen Gerät oder das Zeilen Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**lineerr- \_ invallinestate**</span><span class="sxs-lookup"><span data-stu-id="88173-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-242">Die Gerätekonfiguration kann im aktuellen Zeilen Status nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="88173-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="88173-243">Die Zeile wird möglicherweise von einer anderen Anwendung verwendet, oder ein *dwlinestates* -Parameter enthält mindestens ein Bit, das keine [linedevstate- \_ Konstanten](linedevstate--constants.md)ist.</span><span class="sxs-lookup"><span data-stu-id="88173-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="88173-244">Der **lineerr-Wert " \_ invallinestate** " kann auch darauf hinweisen, dass das Gerät getrennt oder außer Betrieb genommen wird.</span><span class="sxs-lookup"><span data-stu-id="88173-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="88173-245">Diese Zustände werden angegeben, indem die Bits, die den *\_ verbundenen linedevstatusflags* -und *linedevstatusflags- \_ INService* -Werten entsprechen, im **dwdevstatusflags** -Member der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Struktur, die von der [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) -Funktion zurückgegeben wird, auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="88173-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**lineerr \_ invallocation**</span><span class="sxs-lookup"><span data-stu-id="88173-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-247">Der in *dwlocation* angegebene Bezeichner für die permanente Position konnte in keinem Eintrag im Abschnitt "Speicher \[ Orte" \] in der Registrierung gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="88173-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**lineerr \_ invalmedialist**</span><span class="sxs-lookup"><span data-stu-id="88173-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-249">Die angegebene Medien Liste ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**lineerr \_ invalmediamode**</span><span class="sxs-lookup"><span data-stu-id="88173-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-251">Die Liste der zu überwachenden Medientypen (Modi) enthält ungültige Informationen, der angegebene Medientyp-Parameter ist ungültig, oder der angegebene Medientyp wird vom Dienstanbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88173-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="88173-252">Die in der Zeile unterstützten Medientypen werden im **dwmediamodes** -Member in der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="88173-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**lineerr \_ invalmessageid**</span><span class="sxs-lookup"><span data-stu-id="88173-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-254">Die in *dwMessageId* angegebene Zahl liegt außerhalb des Bereichs, der vom **dwnumcompletionmessages** -Member in der [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88173-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**lineerr \_ invalparam**</span><span class="sxs-lookup"><span data-stu-id="88173-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-256">Ein Parameter oder eine Struktur, auf den ein Parameter zeigt, enthält ungültige Informationen, ein Länder-oder Regions Code ist ungültig, ein Fenster Handle ist ungültig, oder der angegebene forward-Listen Parameter enthält ungültige Informationen.</span><span class="sxs-lookup"><span data-stu-id="88173-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**lineerr \_ invalpark ID**</span><span class="sxs-lookup"><span data-stu-id="88173-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-258">Der Park Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**lineerr \_ invalparkmode**</span><span class="sxs-lookup"><span data-stu-id="88173-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-260">Der angegebene Park Modus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**lineerr \_ invalpassword**</span><span class="sxs-lookup"><span data-stu-id="88173-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-262">Das angegebene Kennwort ist nicht korrekt, und die angeforderte Aktion wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88173-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**lineerr \_ invalpassword**</span><span class="sxs-lookup"><span data-stu-id="88173-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-264">Die Anwendung hat ein ungültiges Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="88173-264">The application used an invalid password.</span></span> <span data-ttu-id="88173-265">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**lineerr- \_ invalpointer**</span><span class="sxs-lookup"><span data-stu-id="88173-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-267">Mindestens ein angegebener Zeiger Parameter (z. b. *lpcalllist*, *lpdwapiversion*, *lpextensionid*, *lpdwextversion*, *lphicon*, *lplinedevcaps* und *lptonelist*) ist ungültig, oder ein erforderlicher Zeiger auf einen Output-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="88173-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**lineerr \_ invalprivselect**</span><span class="sxs-lookup"><span data-stu-id="88173-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-269">Für den *dwprivileges* -Parameter wurde ein ungültiges Flag oder eine ungültige Kombination von Flags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88173-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**lineerr- \_ invalate**</span><span class="sxs-lookup"><span data-stu-id="88173-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-271">Die angegebene Rate ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**lineerr \_ invalrequestmode**</span><span class="sxs-lookup"><span data-stu-id="88173-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-273">Der [**linerequestmode**](linerequestmode--constants.md) -Indikator ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**lineerr \_ invalterminalid**</span><span class="sxs-lookup"><span data-stu-id="88173-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-275">Der angegebene Terminal Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**lineerr \_ invalterminalmode**</span><span class="sxs-lookup"><span data-stu-id="88173-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-277">Der angegebene terminalmodusparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**lineerr \_ invaltimeout**</span><span class="sxs-lookup"><span data-stu-id="88173-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-279">Timeouts werden nicht unterstützt, oder ein Wert liegt außerhalb des gültigen Bereichs, der in [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="88173-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**lineerr \_ invaltone**</span><span class="sxs-lookup"><span data-stu-id="88173-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-281">Der angegebene benutzerdefinierte Farbton stellt keinen gültigen Ton dar oder besteht aus zu vielen Frequenzen, oder die angegebene Tonstruktur beschreibt keinen gültigen Ton.</span><span class="sxs-lookup"><span data-stu-id="88173-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**lineerr \_ invaltonelist**</span><span class="sxs-lookup"><span data-stu-id="88173-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-283">Die angegebene Tonliste ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**lineerr \_ invaltonemode**</span><span class="sxs-lookup"><span data-stu-id="88173-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-285">Der angegebene Tone Mode-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**lineerr \_ invaltransfermode**</span><span class="sxs-lookup"><span data-stu-id="88173-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-287">Der angegebene Übertragungsmodus-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="88173-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**lineerr \_ linemapperfailed**</span><span class="sxs-lookup"><span data-stu-id="88173-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-289">Linemapper war der Wert, der im *dwdeviceid* -Parameter übergeben wurde, aber es wurden keine Zeilen gefunden, die den im *lpcallparameams* -Parameter angegebenen Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="88173-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**lineerr \_ noconference**</span><span class="sxs-lookup"><span data-stu-id="88173-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-291">Der angegebene-Befehl ist kein Konferenz-oder Teilnehmer aufrufshandle.</span><span class="sxs-lookup"><span data-stu-id="88173-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**lineerr- \_ nodevice**</span><span class="sxs-lookup"><span data-stu-id="88173-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-293">Der angegebene Geräte Bezeichner, der zuvor gültig war, wird nicht mehr akzeptiert, weil das zugehörige Gerät seit der letzten Initialisierung von TAPI aus dem System entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="88173-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="88173-294">Alternativ weist das liniengerät kein zugeordnetes Gerät für die angegebene Geräteklasse auf.</span><span class="sxs-lookup"><span data-stu-id="88173-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**lineerr- \_ nodriver**</span><span class="sxs-lookup"><span data-stu-id="88173-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-296">Entweder wurde Tapiaddr.dll nicht gefunden, oder der Telefon Dienstanbieter für das angegebene Gerät hat erkannt, dass eine der Komponenten fehlt oder beschädigt ist, weil Sie nicht während der Initialisierung erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="88173-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="88173-297">Der Benutzer sollte aufgefordert werden, das Problem mithilfe der Telefonie-Systemsteuerung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="88173-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**lineerr \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="88173-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-299">Nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs, oder der Arbeitsspeicher kann nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="88173-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**lineerr \_ nomultiplin Stance**</span><span class="sxs-lookup"><span data-stu-id="88173-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-301">Ein Telefoniedienstanbieter, der mehrere Instanzen nicht unterstützt, ist mehrmals im \[ Abschnitt "Anbieter" \] in der Registrierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="88173-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="88173-302">Die Anwendung sollte dem Benutzer die Verwendung der Telefonie-Systemsteuerung zum Entfernen des duplizierten Treibers empfehlen.</span><span class="sxs-lookup"><span data-stu-id="88173-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**lineerr \_ nomultiplin Stance**</span><span class="sxs-lookup"><span data-stu-id="88173-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-304">Mehrere Instanzen dieses Dienstanbieters sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="88173-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**lineerr \_ norequest**</span><span class="sxs-lookup"><span data-stu-id="88173-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-306">Zurzeit steht keine Anforderung aus dem angegebenen Modus aus, oder die Anwendung ist nicht mehr die Anwendung mit der höchsten Priorität für den angegebenen Anforderungs Modus.</span><span class="sxs-lookup"><span data-stu-id="88173-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**lineerr- \_ notowner**</span><span class="sxs-lookup"><span data-stu-id="88173-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-308">Die Anwendung verfügt nicht über die Berechtigung "Besitzer" für den angegebenen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="88173-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**lineerr \_ notregistered**</span><span class="sxs-lookup"><span data-stu-id="88173-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-310">Die Anwendung ist nicht als Anforderungs Empfänger für den angezeigtem Anforderungs Modus registriert.</span><span class="sxs-lookup"><span data-stu-id="88173-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**lineerr- \_ operationfailed**</span><span class="sxs-lookup"><span data-stu-id="88173-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-312">Der Vorgang ist aus einem nicht angegebenen oder unbekannten Grund fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="88173-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**lineerr \_ operationunnütz**</span><span class="sxs-lookup"><span data-stu-id="88173-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-314">Der Vorgang ist nicht verfügbar, z. b. für das angegebene Gerät oder die angegebene Zeile.</span><span class="sxs-lookup"><span data-stu-id="88173-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**lineerr \_ rateun-Anspruch**</span><span class="sxs-lookup"><span data-stu-id="88173-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-316">Der Dienstanbieter verfügt derzeit nicht über genügend Bandbreite für die angegebene Rate.</span><span class="sxs-lookup"><span data-stu-id="88173-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**lineerr \_ Reit**</span><span class="sxs-lookup"><span data-stu-id="88173-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-318">Wenn die TAPI-Neuinitialisierung angefordert wurde, z. b. aufgrund des Hinzufügens oder Entfernens eines Telefoniedienstanbieters, anschließend werden [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)-, [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)-oder [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) -Anforderungen mit diesem Fehler zurückgewiesen, bis die letzte Anwendung die Verwendung der API herunterfährt (mit [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)). zu diesem Zeitpunkt wird die neue Konfiguration wirksam, und Anwendungen können **lineinitialize** oder **lineinitializeex** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="88173-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**lineerr \_ Reit**</span><span class="sxs-lookup"><span data-stu-id="88173-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-320">Die Anwendung hat versucht, TAPI zweimal zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="88173-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**lineerr \_ requestüberlauf**</span><span class="sxs-lookup"><span data-stu-id="88173-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-322">Es stehen weitere Anforderungen aus, die vom Gerät verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="88173-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**lineerr \_ resourceunnütz**</span><span class="sxs-lookup"><span data-stu-id="88173-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-324">Nicht genügend Ressourcen, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="88173-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="88173-325">Beispielsweise kann eine Zeile aufgrund einer dynamischen Ressourcen Übereinstimmung nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**lineerr \_ structureumosmall**</span><span class="sxs-lookup"><span data-stu-id="88173-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-327">Der **dwtotalsize** -Member einer-Struktur gibt nicht genügend Arbeitsspeicher an, um den festgelegten Teil der angegebenen-Struktur zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="88173-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**lineerr \_ targetnotfound**</span><span class="sxs-lookup"><span data-stu-id="88173-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-329">Es wurde kein Ziel für den calloff gefunden.</span><span class="sxs-lookup"><span data-stu-id="88173-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="88173-330">Dies kann vorkommen, wenn die benannte Anwendung nicht dieselbe Zeile mit dem Besitzer des linecallprivilege- \_ Besitzers im *dwprivileges* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="88173-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="88173-331">Im Fall der Medien Modus-Übergabe hat keine Anwendung dieselbe Zeile mit dem Besitzer des linecallprivilege \_ -Besitzers im *dwprivileges* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) geöffnet, und der im *dwmediamode* -Parameter angegebene Medientyp wurde im *dwmediamodes* -Parameter von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)angegeben.</span><span class="sxs-lookup"><span data-stu-id="88173-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**lineerr \_ targetSelf**</span><span class="sxs-lookup"><span data-stu-id="88173-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-333">Die Anwendung, die diesen Vorgang aufruft, ist das Ziel der indirekten Übergabe.</span><span class="sxs-lookup"><span data-stu-id="88173-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="88173-334">Das heißt, TAPI hat festgestellt, dass die aufrufenden Anwendung auch die Anwendung mit der höchsten Priorität für den angegebenen Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="88173-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**lineerr \_ nicht initialisiert**</span><span class="sxs-lookup"><span data-stu-id="88173-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-336">Der Vorgang wurde vor einer Anwendung mit dem Namen [**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) oder [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="88173-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**lineerr- \_ Benutzer abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="88173-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-338">Der Benutzer hat den-Befehl abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="88173-338">The user cancelled the call.</span></span> <span data-ttu-id="88173-339">Dieser Wert ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,2 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88173-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**lineerr \_ useruserinfotoobig**</span><span class="sxs-lookup"><span data-stu-id="88173-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88173-341">Die Zeichenfolge, die Benutzer Benutzerinformationen enthält, überschreitet die maximale Anzahl von Bytes, die in den Elementen **dwuuiakzeptsize**, **dwuuibeantworsize**, **dwuuidropsize**, **dwuuimakecallsize** oder **dwuuisenduseruserinfosize** von [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)angegeben sind, oder die Zeichenfolge, die Benutzer Benutzerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="88173-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88173-342">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88173-342">Remarks</span></span>

<span data-ttu-id="88173-343">Die Werte 0xC0000000 bis 0xffffffff sind für gerätespezifische Erweiterungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88173-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="88173-344">Die Werte 0x80000000 bis 0xBFFFFFFF sind reserviert, während 0x00000000 bis 0x7FFFFFFF als Anforderungs Bezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88173-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="88173-345">Wenn eine Anwendung eine Fehlermeldung erhält, die Sie nicht speziell behandelt (z. b. einen Fehler, der durch eine gerätespezifische Erweiterung definiert wurde), sollte Sie den Fehler als lineerr \_ operationfailed (aus einem nicht angegebenen Grund) behandeln.</span><span class="sxs-lookup"><span data-stu-id="88173-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="88173-346">Beim Aufrufen der lineerr- \_ Konstanten, die neu bei TAPI 3,0 sind, muss die Datei Tapierr.MC mit neuen Nachrichten aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="88173-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="88173-347">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88173-347">Requirements</span></span>



| <span data-ttu-id="88173-348">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88173-348">Requirement</span></span> | <span data-ttu-id="88173-349">Wert</span><span class="sxs-lookup"><span data-stu-id="88173-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88173-350">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="88173-350">TAPI version</span></span><br/> | <span data-ttu-id="88173-351">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="88173-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="88173-352">Header</span><span class="sxs-lookup"><span data-stu-id="88173-352">Header</span></span><br/>       | <dl> <span data-ttu-id="88173-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="88173-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88173-354">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88173-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88173-355">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="88173-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="88173-356">**Linedevcaps**</span><span class="sxs-lookup"><span data-stu-id="88173-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="88173-357">**Linedevstatus**</span><span class="sxs-lookup"><span data-stu-id="88173-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="88173-358">**linegetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="88173-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="88173-359">**lineinitialize**</span><span class="sxs-lookup"><span data-stu-id="88173-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="88173-360">**lineinitializeex**</span><span class="sxs-lookup"><span data-stu-id="88173-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="88173-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="88173-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="88173-362">**LineShutdown**</span><span class="sxs-lookup"><span data-stu-id="88173-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




