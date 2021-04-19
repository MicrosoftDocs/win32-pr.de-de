---
description: Die grundlegenden Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Grundlegende telefoniedienstreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348289"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="45cf3-103">Grundlegende telefoniedienstreferenz</span><span class="sxs-lookup"><span data-stu-id="45cf3-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="45cf3-104">Die grundlegenden Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45cf3-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="45cf3-105">Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="45cf3-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="45cf3-106">Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="45cf3-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="45cf3-107">Im folgenden finden Sie eine funktionale Gruppierung der grundlegenden telefoniedienstfunktionen:</span><span class="sxs-lookup"><span data-stu-id="45cf3-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="45cf3-108">Adressformate</span><span class="sxs-lookup"><span data-stu-id="45cf3-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="45cf3-109">Adresses</span><span class="sxs-lookup"><span data-stu-id="45cf3-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="45cf3-110">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="45cf3-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="45cf3-111">Drop Functions-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="45cf3-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="45cf3-112">Bearbeitung von anrufhandles</span><span class="sxs-lookup"><span data-stu-id="45cf3-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="45cf3-113">Berechtigungs Steuerelement anrufen</span><span class="sxs-lookup"><span data-stu-id="45cf3-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="45cf3-114">Aufrufe von Zuständen und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="45cf3-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="45cf3-115">Zeilen Status und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="45cf3-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="45cf3-116">Aushandlung der Zeilen Version</span><span class="sxs-lookup"><span data-stu-id="45cf3-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="45cf3-117">Standort-und Land/Region-Informationen</span><span class="sxs-lookup"><span data-stu-id="45cf3-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="45cf3-118">Aufrufen</span><span class="sxs-lookup"><span data-stu-id="45cf3-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="45cf3-119">Öffnen und Schließen von Linien Geräten</span><span class="sxs-lookup"><span data-stu-id="45cf3-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="45cf3-120">Empfänger Dienste anfordern</span><span class="sxs-lookup"><span data-stu-id="45cf3-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="45cf3-121">TAPI-Initialisierung und-Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="45cf3-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="45cf3-122">Unterstützung für Maut Sparer</span><span class="sxs-lookup"><span data-stu-id="45cf3-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="45cf3-123">TAPI-Initialisierung und-Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="45cf3-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="45cf3-124">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-124">Function</span></span>                                     | <span data-ttu-id="45cf3-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-126">**lineinitializeex**</span><span class="sxs-lookup"><span data-stu-id="45cf3-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="45cf3-127">Initialisiert die TAPI-Zeilen Abstraktion, die von der Aufruf Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45cf3-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="45cf3-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-128">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-129">**LineShutdown**</span><span class="sxs-lookup"><span data-stu-id="45cf3-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="45cf3-130">Schaltet die Verwendung der TAPI-Zeilen Abstraktion durch die Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="45cf3-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="45cf3-131">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="45cf3-132">Aushandlung der Zeilen Version</span><span class="sxs-lookup"><span data-stu-id="45cf3-132">Line Version Negotiation</span></span>



| <span data-ttu-id="45cf3-133">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-133">Function</span></span>                                                   | <span data-ttu-id="45cf3-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="45cf3-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="45cf3-136">Ermöglicht es einer Anwendung, eine TAPI-Version für die Verwendung von auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="45cf3-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="45cf3-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="45cf3-138">Zeilen Status und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="45cf3-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="45cf3-139">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-139">Function</span></span>                                               | <span data-ttu-id="45cf3-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-141">**linegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="45cf3-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="45cf3-142">Gibt die Funktionen eines angegebenen Zeilen Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="45cf3-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="45cf3-144">**linegetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="45cf3-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="45cf3-145">Gibt die Konfiguration eines Medienstrom Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="45cf3-146">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="45cf3-147">**linegetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="45cf3-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="45cf3-148">Gibt den aktuellen Status des angegebenen Open-Line-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="45cf3-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="45cf3-150">**linesetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="45cf3-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="45cf3-151">Legt die Konfiguration des angegebenen Medienstrom Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="45cf3-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="45cf3-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="45cf3-153">**linesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="45cf3-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="45cf3-154">Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="45cf3-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="45cf3-155">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="45cf3-156">**linegetstatus Messages**</span><span class="sxs-lookup"><span data-stu-id="45cf3-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="45cf3-157">Gibt die aktuellen Zeilen-und Adress Status Meldungs Einstellungen der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="45cf3-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="45cf3-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="45cf3-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="45cf3-160">Ruft eine Geräte-ID ab, die der angegebenen öffnenden Zeile, Adresse oder dem angegebenen-Befehl zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="45cf3-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="45cf3-161">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="45cf3-162">**linegeticon**</span><span class="sxs-lookup"><span data-stu-id="45cf3-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="45cf3-163">Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="45cf3-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="45cf3-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="45cf3-165">**lineconfigdialog**</span><span class="sxs-lookup"><span data-stu-id="45cf3-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="45cf3-166">Bewirkt, dass der Anbieter des angegebenen Zeilen Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem liniengerät zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="45cf3-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="45cf3-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-167">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-168">**lineconfigdialogedit**</span><span class="sxs-lookup"><span data-stu-id="45cf3-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="45cf3-169">Zeigt ein Dialogfeld an, in dem der Benutzer Konfigurationsinformationen für ein liniengerät ändern kann.</span><span class="sxs-lookup"><span data-stu-id="45cf3-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="45cf3-170">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="45cf3-171">Adressen</span><span class="sxs-lookup"><span data-stu-id="45cf3-171">Addresses</span></span>



| <span data-ttu-id="45cf3-172">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-172">Function</span></span>                                             | <span data-ttu-id="45cf3-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-174">**linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="45cf3-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="45cf3-175">Gibt die Telefoniefunktionen einer Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="45cf3-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="45cf3-177">**linegetaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="45cf3-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="45cf3-178">Gibt den aktuellen Status einer angegebenen Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-178">Returns current status of a specified address.</span></span> <span data-ttu-id="45cf3-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="45cf3-180">**linegetadressssid**</span><span class="sxs-lookup"><span data-stu-id="45cf3-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="45cf3-181">Ruft die Adress-ID einer Adresse ab, die mit einem alternativen Format angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="45cf3-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="45cf3-182">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="45cf3-183">Öffnen und Schließen von Linien Geräten</span><span class="sxs-lookup"><span data-stu-id="45cf3-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="45cf3-184">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-184">Function</span></span>                       | <span data-ttu-id="45cf3-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="45cf3-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="45cf3-187">Öffnet ein angegebenes Zeilen Gerät zum Bereitstellen der nachfolgenden Überwachung und/oder Steuerung der Zeile.</span><span class="sxs-lookup"><span data-stu-id="45cf3-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="45cf3-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-188">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-189">**lineclose**</span><span class="sxs-lookup"><span data-stu-id="45cf3-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="45cf3-190">Schließt ein angegebenes geöffnetes Zeilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="45cf3-190">Closes a specified opened line device.</span></span> <span data-ttu-id="45cf3-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="45cf3-192">Adressformate</span><span class="sxs-lookup"><span data-stu-id="45cf3-192">Address Formats</span></span>



| <span data-ttu-id="45cf3-193">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-193">Function</span></span>                                                 | <span data-ttu-id="45cf3-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-195">**linetranslateaddress**</span><span class="sxs-lookup"><span data-stu-id="45cf3-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="45cf3-196">Übersetzt eine Adresse im kanonischen Format und eine Adresse im ddbaren Format.</span><span class="sxs-lookup"><span data-stu-id="45cf3-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="45cf3-197">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-197">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-198">**linesetcurrentlocation**</span><span class="sxs-lookup"><span data-stu-id="45cf3-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="45cf3-199">Legt den Speicherort fest, der als Kontext für die Adressübersetzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45cf3-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="45cf3-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="45cf3-201">**linesettolllist**</span><span class="sxs-lookup"><span data-stu-id="45cf3-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="45cf3-202">Bearbeitet die Maut Liste.</span><span class="sxs-lookup"><span data-stu-id="45cf3-202">Manipulates the toll list.</span></span> <span data-ttu-id="45cf3-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="45cf3-204">**linegettranslatecaps**</span><span class="sxs-lookup"><span data-stu-id="45cf3-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="45cf3-205">Gibt Adress Übersetzungsfunktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-205">Returns address translation capabilities.</span></span> <span data-ttu-id="45cf3-206">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="45cf3-207">Aufrufe von Zuständen und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="45cf3-207">Call States and Events</span></span>



| <span data-ttu-id="45cf3-208">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-208">Function</span></span>                                         | <span data-ttu-id="45cf3-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-210">**linegetcallinfo**</span><span class="sxs-lookup"><span data-stu-id="45cf3-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="45cf3-211">Gibt fixierte Informationen zu einem-Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-211">Returns fixed information about a call.</span></span> <span data-ttu-id="45cf3-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="45cf3-213">**linegetcallstatus**</span><span class="sxs-lookup"><span data-stu-id="45cf3-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="45cf3-214">Gibt die Statusinformationen zum Abschluss des angegebenen Aufrufes zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="45cf3-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-215">Synchronous.</span></span>       |
| [<span data-ttu-id="45cf3-216">**linesetappspecific**</span><span class="sxs-lookup"><span data-stu-id="45cf3-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="45cf3-217">Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufes fest.</span><span class="sxs-lookup"><span data-stu-id="45cf3-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="45cf3-218">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="45cf3-219">Aufrufen</span><span class="sxs-lookup"><span data-stu-id="45cf3-219">Making Calls</span></span>



| <span data-ttu-id="45cf3-220">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-220">Function</span></span>                             | <span data-ttu-id="45cf3-221">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-222">**linemakecall**</span><span class="sxs-lookup"><span data-stu-id="45cf3-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="45cf3-223">Führt einen ausgehenden-Rückruf aus und gibt ein-Rückruf handle dafür zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="45cf3-224">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="45cf3-224">Asynchronous.</span></span> |
| [<span data-ttu-id="45cf3-225">**linedial**</span><span class="sxs-lookup"><span data-stu-id="45cf3-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="45cf3-226">Dials (Teile von einer oder mehreren), die als nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="45cf3-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="45cf3-227">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="45cf3-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="45cf3-228">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="45cf3-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="45cf3-229">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-229">Function</span></span>                         | <span data-ttu-id="45cf3-230">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="45cf3-231">**lineanswer**</span><span class="sxs-lookup"><span data-stu-id="45cf3-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="45cf3-232">Beantwortet einen eingehenden-Befehl.</span><span class="sxs-lookup"><span data-stu-id="45cf3-232">Answers an incoming call.</span></span> <span data-ttu-id="45cf3-233">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="45cf3-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="45cf3-234">Unterstützung für Maut Sparer</span><span class="sxs-lookup"><span data-stu-id="45cf3-234">Toll Saver Support</span></span>



| <span data-ttu-id="45cf3-235">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-235">Function</span></span>                                   | <span data-ttu-id="45cf3-236">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-237">**linesetnumrings**</span><span class="sxs-lookup"><span data-stu-id="45cf3-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="45cf3-238">Gibt die Anzahl der Ringe an, nach denen eingehende Aufrufe beantwortet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45cf3-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="45cf3-239">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="45cf3-240">**linegetnumrings**</span><span class="sxs-lookup"><span data-stu-id="45cf3-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="45cf3-241">Gibt die Mindestanzahl der mit [**linesetnumrings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings)angeforderten Ringe zurück.</span><span class="sxs-lookup"><span data-stu-id="45cf3-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="45cf3-242">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="45cf3-243">Berechtigungs Steuerelement anrufen</span><span class="sxs-lookup"><span data-stu-id="45cf3-243">Call Privilege Control</span></span>



| <span data-ttu-id="45cf3-244">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-244">Function</span></span>                                             | <span data-ttu-id="45cf3-245">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-246">**linesetcallprivilege**</span><span class="sxs-lookup"><span data-stu-id="45cf3-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="45cf3-247">Legt die Berechtigung der Anwendung auf das angegebene Privileg fest.</span><span class="sxs-lookup"><span data-stu-id="45cf3-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="45cf3-248">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="45cf3-249">Drop Functions-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="45cf3-249">Call Drop Functions</span></span>



| <span data-ttu-id="45cf3-250">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-250">Function</span></span>                                         | <span data-ttu-id="45cf3-251">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-252">**linedrop**</span><span class="sxs-lookup"><span data-stu-id="45cf3-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="45cf3-253">Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="45cf3-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="45cf3-254">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="45cf3-254">Asynchronous.</span></span> |
| [<span data-ttu-id="45cf3-255">**linedezugewiesene eCall**</span><span class="sxs-lookup"><span data-stu-id="45cf3-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="45cf3-256">Hebt die Zuordnung des angegebenen-Rückruf Handles auf.</span><span class="sxs-lookup"><span data-stu-id="45cf3-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="45cf3-257">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="45cf3-258">Bearbeitung von anrufhandles</span><span class="sxs-lookup"><span data-stu-id="45cf3-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="45cf3-259">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-259">Function</span></span>                                                   | <span data-ttu-id="45cf3-260">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-261">**linehandoff**</span><span class="sxs-lookup"><span data-stu-id="45cf3-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="45cf3-262">Übergibt den Besitz von Anrufen und/oder ändert die Berechtigungen einer Anwendung in einen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="45cf3-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="45cf3-263">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="45cf3-264">**linegetnewcalls**</span><span class="sxs-lookup"><span data-stu-id="45cf3-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="45cf3-265">Gibt Aufruf Handles zum Aufrufen einer angegebenen Zeile oder Adresse zurück, für die die Anwendung noch keine Handles hat.</span><span class="sxs-lookup"><span data-stu-id="45cf3-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="45cf3-266">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-266">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-267">**lineget-frelatedcalls**</span><span class="sxs-lookup"><span data-stu-id="45cf3-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="45cf3-268">Gibt eine Liste von aufrufhandles zurück, die Teil desselben Konferenz Aufrufes sind wie der als Parameter angegebene-Befehl.</span><span class="sxs-lookup"><span data-stu-id="45cf3-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="45cf3-269">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="45cf3-270">Standort-und Land/Region-Informationen</span><span class="sxs-lookup"><span data-stu-id="45cf3-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="45cf3-271">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-271">Function</span></span>                                           | <span data-ttu-id="45cf3-272">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-273">**linetranslatedialog**</span><span class="sxs-lookup"><span data-stu-id="45cf3-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="45cf3-274">Zeigt ein Dialogfeld an, in dem der Benutzer den Speicherort und die Aufruf Karteninformationen ändern kann.</span><span class="sxs-lookup"><span data-stu-id="45cf3-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="45cf3-275">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-275">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-276">**linegetcountry**</span><span class="sxs-lookup"><span data-stu-id="45cf3-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="45cf3-277">Ruft Wähl Regeln und andere Informationen zu einem bestimmten Land oder einer bestimmten Region ab.</span><span class="sxs-lookup"><span data-stu-id="45cf3-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="45cf3-278">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="45cf3-279">Empfänger Dienste anfordern</span><span class="sxs-lookup"><span data-stu-id="45cf3-279">Request Recipient Services</span></span>

<span data-ttu-id="45cf3-280">Die folgenden zwei Funktionen werden nur zur Unterstützung von unterstützten Telefoniefunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="45cf3-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="45cf3-281">Funktion</span><span class="sxs-lookup"><span data-stu-id="45cf3-281">Function</span></span>                                                             | <span data-ttu-id="45cf3-282">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45cf3-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45cf3-283">**lineregisterrequestrecipient**</span><span class="sxs-lookup"><span data-stu-id="45cf3-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="45cf3-284">Registriert oder hebt die Registrierung der Anwendung als Anforderungs Empfänger für den angegebenen Anforderungs Modus auf.</span><span class="sxs-lookup"><span data-stu-id="45cf3-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="45cf3-285">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-285">Synchronous.</span></span> |
| [<span data-ttu-id="45cf3-286">**linegetrequest**</span><span class="sxs-lookup"><span data-stu-id="45cf3-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="45cf3-287">Ruft die nächste Anforderung aus der telefoniebibliothek für dynamische links ab.</span><span class="sxs-lookup"><span data-stu-id="45cf3-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="45cf3-288">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="45cf3-288">Synchronous.</span></span>                                  |



 

 

 



