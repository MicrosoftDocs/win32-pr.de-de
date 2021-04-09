---
description: Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Grundlegende Telefoniefunktionen von TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868599"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="f2c62-103">Grundlegende Telefoniefunktionen von TSPI</span><span class="sxs-lookup"><span data-stu-id="f2c62-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="f2c62-104">Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f2c62-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="f2c62-105">Im folgenden finden Sie eine Liste dieser Funktionen nach Kategorie.</span><span class="sxs-lookup"><span data-stu-id="f2c62-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="f2c62-106">Eine Funktion wird als *asynchron* identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="f2c62-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="f2c62-107">Wenn die Funktion das Ergebnis immer sofort zurückgibt, wird die Funktion als *synchron* betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f2c62-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="f2c62-108">Adresses</span><span class="sxs-lookup"><span data-stu-id="f2c62-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="f2c62-109">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="f2c62-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="f2c62-110">Drop Functions-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="f2c62-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="f2c62-111">Aufrufe von Zuständen und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f2c62-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="f2c62-112">Zeilen Status und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f2c62-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="f2c62-113">Aushandlung der Zeilen Version</span><span class="sxs-lookup"><span data-stu-id="f2c62-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="f2c62-114">Aufrufen</span><span class="sxs-lookup"><span data-stu-id="f2c62-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="f2c62-115">Öffnen und Schließen von Linien Geräten</span><span class="sxs-lookup"><span data-stu-id="f2c62-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="f2c62-116">Aushandlung der Telefon Version</span><span class="sxs-lookup"><span data-stu-id="f2c62-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="f2c62-117">TSP-Initialisierung und-Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="f2c62-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="f2c62-118">TSP-Initialisierung und-Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="f2c62-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="f2c62-119">**Tuispi \_ providerinstall**</span><span class="sxs-lookup"><span data-stu-id="f2c62-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="f2c62-120">Installiert einen TSP.</span><span class="sxs-lookup"><span data-stu-id="f2c62-120">Installs a TSP.</span></span> <span data-ttu-id="f2c62-121">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="f2c62-122">**TSPI \_ providerinstall**</span><span class="sxs-lookup"><span data-stu-id="f2c62-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="f2c62-123">Installiert den TSP.</span><span class="sxs-lookup"><span data-stu-id="f2c62-123">Installs the TSP.</span></span> <span data-ttu-id="f2c62-124">Veraltet mit Version 2,0.</span><span class="sxs-lookup"><span data-stu-id="f2c62-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="f2c62-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-125">Synchronous.</span></span> |
| [<span data-ttu-id="f2c62-126">**TSPI \_ providerinit**</span><span class="sxs-lookup"><span data-stu-id="f2c62-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="f2c62-127">Initialisiert den TSP.</span><span class="sxs-lookup"><span data-stu-id="f2c62-127">Initializes the TSP.</span></span> <span data-ttu-id="f2c62-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="f2c62-129">**TSPI \_ providershutdown**</span><span class="sxs-lookup"><span data-stu-id="f2c62-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="f2c62-130">Fährt den Dienstanbieter herunter.</span><span class="sxs-lookup"><span data-stu-id="f2c62-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="f2c62-131">**Tuispi \_ providerremove**</span><span class="sxs-lookup"><span data-stu-id="f2c62-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="f2c62-132">Entfernt einen TSP.</span><span class="sxs-lookup"><span data-stu-id="f2c62-132">Removes a TSP.</span></span> <span data-ttu-id="f2c62-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="f2c62-134">**TSPI \_ providerremove**</span><span class="sxs-lookup"><span data-stu-id="f2c62-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="f2c62-135">Entfernt einen TSP.</span><span class="sxs-lookup"><span data-stu-id="f2c62-135">Removes a TSP.</span></span> <span data-ttu-id="f2c62-136">Veraltet mit Version 2,0.</span><span class="sxs-lookup"><span data-stu-id="f2c62-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="f2c62-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="f2c62-138">Aushandlung der Telefon Version</span><span class="sxs-lookup"><span data-stu-id="f2c62-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-139">**TSPI \_ phonenegotiatetspiversion**</span><span class="sxs-lookup"><span data-stu-id="f2c62-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="f2c62-140">Gibt die höchste SPI-Version zurück, unter der der Dienstanbieter für dieses Gerät arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f2c62-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="f2c62-141">Aushandlung der Zeilen Version</span><span class="sxs-lookup"><span data-stu-id="f2c62-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-142">**TSPI \_ linenegotiatetspiversion**</span><span class="sxs-lookup"><span data-stu-id="f2c62-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="f2c62-143">Ermöglicht es einer Anwendung, eine TSPI-Version zu aushandeln, die mit einem bestimmten liniengerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2c62-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="f2c62-144">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="f2c62-145">Zeilen Status und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f2c62-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-146">**TSPI \_ linegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="f2c62-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="f2c62-147">Gibt die Funktionen eines angegebenen Zeilen Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="f2c62-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="f2c62-149">**TSPI \_ linegetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="f2c62-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="f2c62-150">Gibt die Konfiguration eines Medienstrom Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="f2c62-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="f2c62-152">**TSPI \_ linegetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="f2c62-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="f2c62-153">Gibt den aktuellen Status des angegebenen Open-Line-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="f2c62-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="f2c62-155">**TSPI \_ linesetdevconfig**</span><span class="sxs-lookup"><span data-stu-id="f2c62-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="f2c62-156">Legt die Konfiguration des angegebenen Medienstrom Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="f2c62-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="f2c62-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="f2c62-158">**TSPI- \_ linesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="f2c62-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="f2c62-159">Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f2c62-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="f2c62-160">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="f2c62-161">**TSPI- \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="f2c62-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="f2c62-162">Ruft eine Geräte-ID ab, die der angegebenen öffnenden Zeile, Adresse oder dem angegebenen-Befehl zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2c62-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="f2c62-163">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="f2c62-164">**TSPI- \_ linegeticon**</span><span class="sxs-lookup"><span data-stu-id="f2c62-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="f2c62-165">Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f2c62-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="f2c62-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="f2c62-167">**Tuispi \_ lineconfigdialog**</span><span class="sxs-lookup"><span data-stu-id="f2c62-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="f2c62-168">Bewirkt, dass der Anbieter des angegebenen Zeilen Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem liniengerät zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f2c62-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="f2c62-169">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-169">Synchronous.</span></span> |
| [<span data-ttu-id="f2c62-170">**Tuispi \_ lineconfigdialogedit**</span><span class="sxs-lookup"><span data-stu-id="f2c62-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="f2c62-171">Zeigt ein Dialogfeld an, in dem der Benutzer Konfigurationsinformationen für ein liniengerät ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f2c62-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="f2c62-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="f2c62-173">Adressen</span><span class="sxs-lookup"><span data-stu-id="f2c62-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-174">**TSPI \_ linegetaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="f2c62-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="f2c62-175">Gibt die Telefoniefunktionen einer Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="f2c62-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="f2c62-177">**TSPI \_ linegetaddressstatus**</span><span class="sxs-lookup"><span data-stu-id="f2c62-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="f2c62-178">Gibt den aktuellen Status einer angegebenen Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-178">Returns current status of a specified address.</span></span> <span data-ttu-id="f2c62-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="f2c62-180">**TSPI \_ linegetnumaddressids**</span><span class="sxs-lookup"><span data-stu-id="f2c62-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="f2c62-181">Ruft die Anzahl der auf der angegebene Zeile unterstützten Adress Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="f2c62-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="f2c62-182">**TSPI \_ linegetadressssid**</span><span class="sxs-lookup"><span data-stu-id="f2c62-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="f2c62-183">Ruft die Adress-ID einer Adresse ab, die mit einem alternativen Format angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2c62-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="f2c62-184">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="f2c62-185">Öffnen und Schließen von Linien Geräten</span><span class="sxs-lookup"><span data-stu-id="f2c62-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-186">**TSPI ( \_ lineOpen)**</span><span class="sxs-lookup"><span data-stu-id="f2c62-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="f2c62-187">Öffnet ein angegebenes Zeilen Gerät zum Bereitstellen der nachfolgenden Überwachung und/oder Steuerung der Zeile.</span><span class="sxs-lookup"><span data-stu-id="f2c62-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="f2c62-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-188">Synchronous.</span></span> |
| [<span data-ttu-id="f2c62-189">**TSPI- \_ lineclose**</span><span class="sxs-lookup"><span data-stu-id="f2c62-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="f2c62-190">Schließt ein angegebenes geöffnetes Zeilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="f2c62-190">Closes a specified opened line device.</span></span> <span data-ttu-id="f2c62-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="f2c62-192">Aufrufe von Zuständen und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="f2c62-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-193">**TSPI \_ linegetcallinfo**</span><span class="sxs-lookup"><span data-stu-id="f2c62-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="f2c62-194">Gibt fixierte Informationen zu einem-Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-194">Returns fixed information about a call.</span></span> <span data-ttu-id="f2c62-195">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="f2c62-196">**TSPI \_ linegetcallstatus**</span><span class="sxs-lookup"><span data-stu-id="f2c62-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="f2c62-197">Gibt die Statusinformationen zum Abschluss des angegebenen Aufrufes zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="f2c62-198">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-198">Synchronous.</span></span>       |
| [<span data-ttu-id="f2c62-199">**TSPI \_ linesetappspecific**</span><span class="sxs-lookup"><span data-stu-id="f2c62-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="f2c62-200">Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufes fest.</span><span class="sxs-lookup"><span data-stu-id="f2c62-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="f2c62-201">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="f2c62-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="f2c62-202">Aufrufen</span><span class="sxs-lookup"><span data-stu-id="f2c62-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-203">**TSPI \_ linemakecall**</span><span class="sxs-lookup"><span data-stu-id="f2c62-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="f2c62-204">Führt einen ausgehenden-Rückruf aus und gibt ein-Rückruf handle dafür zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c62-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="f2c62-205">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="f2c62-205">Asynchronous.</span></span> |
| [<span data-ttu-id="f2c62-206">**TSPI- \_ linedial**</span><span class="sxs-lookup"><span data-stu-id="f2c62-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="f2c62-207">Dials (Teile von einer oder mehreren), die als nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f2c62-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="f2c62-208">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="f2c62-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="f2c62-209">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="f2c62-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="f2c62-210">**TSPI- \_ lineanswer**</span><span class="sxs-lookup"><span data-stu-id="f2c62-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="f2c62-211">Beantwortet einen eingehenden-Befehl.</span><span class="sxs-lookup"><span data-stu-id="f2c62-211">Answers an incoming call.</span></span> <span data-ttu-id="f2c62-212">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="f2c62-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="f2c62-213">Drop Functions-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="f2c62-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="f2c62-214">**TSPI- \_ linedrop**</span><span class="sxs-lookup"><span data-stu-id="f2c62-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="f2c62-215">Trennt einen-Befehl oder bricht einen aufzurufenden Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="f2c62-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="f2c62-216">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="f2c62-216">Asynchronous.</span></span> |



 

 

 
