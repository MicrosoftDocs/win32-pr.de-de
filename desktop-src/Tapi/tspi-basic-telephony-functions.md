---
description: Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: GRUNDLEGENDE TSPI-Telefoniefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524154"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="ceaea-103">GRUNDLEGENDE TSPI-Telefoniefunktionen</span><span class="sxs-lookup"><span data-stu-id="ceaea-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="ceaea-104">Alle Dienstanbieter müssen grundlegende Telefoniefunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="ceaea-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="ceaea-105">Im Folgenden finden Sie eine Liste solcher Funktionen nach Kategorie.</span><span class="sxs-lookup"><span data-stu-id="ceaea-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="ceaea-106">Eine Funktion wird als asynchron *identifiziert,* wenn sie die Vervollständigung in einer ANTWORT-Nachricht an die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="ceaea-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="ceaea-107">Wenn die Funktion ihr Ergebnis immer sofort zurückgibt, wird die Funktion als synchron *betrachtet.*</span><span class="sxs-lookup"><span data-stu-id="ceaea-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="ceaea-108">Adresses</span><span class="sxs-lookup"><span data-stu-id="ceaea-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="ceaea-109">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="ceaea-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="ceaea-110">Drop-Funktionen für Aufrufe</span><span class="sxs-lookup"><span data-stu-id="ceaea-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="ceaea-111">Aufrufzustände und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ceaea-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="ceaea-112">Zeilenstatus und Funktionen</span><span class="sxs-lookup"><span data-stu-id="ceaea-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="ceaea-113">Zeilenversionsaushandlung</span><span class="sxs-lookup"><span data-stu-id="ceaea-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="ceaea-114">Tätigen von Aufrufen</span><span class="sxs-lookup"><span data-stu-id="ceaea-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="ceaea-115">Öffnen und Schließen von Line-Geräten</span><span class="sxs-lookup"><span data-stu-id="ceaea-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="ceaea-116">Telefonversionsaushandlung</span><span class="sxs-lookup"><span data-stu-id="ceaea-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="ceaea-117">TSP-Initialisierung und -Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="ceaea-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="ceaea-118">TSP-Initialisierung und -Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="ceaea-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="ceaea-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-119">Function</span></span>                                                         |   <span data-ttu-id="ceaea-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="ceaea-121">**\_PROVIDERSPI-AnbieterInstallieren**</span><span class="sxs-lookup"><span data-stu-id="ceaea-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="ceaea-122">Installiert einen TSP.</span><span class="sxs-lookup"><span data-stu-id="ceaea-122">Installs a TSP.</span></span> <span data-ttu-id="ceaea-123">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="ceaea-124">**\_TSPI-AnbieterInstallieren**</span><span class="sxs-lookup"><span data-stu-id="ceaea-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="ceaea-125">Installiert den TSP.</span><span class="sxs-lookup"><span data-stu-id="ceaea-125">Installs the TSP.</span></span> <span data-ttu-id="ceaea-126">Veraltet mit Version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ceaea-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="ceaea-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-127">Synchronous.</span></span> |
| [<span data-ttu-id="ceaea-128">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="ceaea-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="ceaea-129">Initialisiert den TSP.</span><span class="sxs-lookup"><span data-stu-id="ceaea-129">Initializes the TSP.</span></span> <span data-ttu-id="ceaea-130">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="ceaea-131">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="ceaea-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="ceaea-132">Fährt den Dienstanbieter herunter.</span><span class="sxs-lookup"><span data-stu-id="ceaea-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="ceaea-133">**PROVIDERSSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="ceaea-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="ceaea-134">Entfernt einen TSP.</span><span class="sxs-lookup"><span data-stu-id="ceaea-134">Removes a TSP.</span></span> <span data-ttu-id="ceaea-135">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="ceaea-136">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="ceaea-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="ceaea-137">Entfernt einen TSP.</span><span class="sxs-lookup"><span data-stu-id="ceaea-137">Removes a TSP.</span></span> <span data-ttu-id="ceaea-138">Veraltet mit Version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ceaea-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="ceaea-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="ceaea-140">Telefonversionsaushandlung</span><span class="sxs-lookup"><span data-stu-id="ceaea-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="ceaea-141">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-141">Function</span></span>                                                         |   <span data-ttu-id="ceaea-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-143">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="ceaea-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="ceaea-144">Gibt die höchste SPI-Version zurück, unter der der Dienstanbieter für dieses Gerät arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="ceaea-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="ceaea-145">Zeilenversionsaushandlung</span><span class="sxs-lookup"><span data-stu-id="ceaea-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="ceaea-146">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-146">Function</span></span>                                                         |   <span data-ttu-id="ceaea-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-148">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="ceaea-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="ceaea-149">Ermöglicht einer Anwendung das Aushandeln einer TSPI-Version für die Verwendung mit einem bestimmten Liniengerät.</span><span class="sxs-lookup"><span data-stu-id="ceaea-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="ceaea-150">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="ceaea-151">Zeilenstatus und Funktionen</span><span class="sxs-lookup"><span data-stu-id="ceaea-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="ceaea-152">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-152">Function</span></span>                                                         |   <span data-ttu-id="ceaea-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-154">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ceaea-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="ceaea-155">Gibt die Funktionen eines bestimmten Liniengeräts zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="ceaea-156">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="ceaea-157">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="ceaea-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="ceaea-158">Gibt die Konfiguration eines Medienstreamgeräts zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="ceaea-159">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="ceaea-160">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ceaea-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="ceaea-161">Gibt den aktuellen Status des angegebenen Open Line-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="ceaea-162">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="ceaea-163">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="ceaea-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="ceaea-164">Legt die Konfiguration des angegebenen Medienstreamgeräts fest.</span><span class="sxs-lookup"><span data-stu-id="ceaea-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="ceaea-165">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="ceaea-166">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="ceaea-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="ceaea-167">Gibt die Statusänderungen an, bei denen die Anwendung benachrichtigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ceaea-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="ceaea-168">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="ceaea-169">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="ceaea-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="ceaea-170">Ruft eine Geräte-ID ab, die der angegebenen offenen Zeile, Adresse oder dem angegebenen Aufruf zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ceaea-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="ceaea-171">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="ceaea-172">**\_TSPI-ZeileGetIcon**</span><span class="sxs-lookup"><span data-stu-id="ceaea-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="ceaea-173">Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ceaea-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="ceaea-174">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="ceaea-175">**KONSTRUKTORSPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="ceaea-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="ceaea-176">Veranlasst den Anbieter des angegebenen Liniengeräts, ein Dialogfeld anzuzeigen, in dem der Benutzer Parameter konfigurieren kann, die sich auf das Liniengerät bezieht.</span><span class="sxs-lookup"><span data-stu-id="ceaea-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="ceaea-177">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-177">Synchronous.</span></span> |
| [<span data-ttu-id="ceaea-178">**KONSTRUKTORSPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="ceaea-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="ceaea-179">Zeigt ein Dialogfeld an, in dem der Benutzer konfigurationsinformationen für ein Liniengerät ändern kann.</span><span class="sxs-lookup"><span data-stu-id="ceaea-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="ceaea-180">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="ceaea-181">Adressen</span><span class="sxs-lookup"><span data-stu-id="ceaea-181">Addresses</span></span>



|  <span data-ttu-id="ceaea-182">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-182">Function</span></span>                                                         |   <span data-ttu-id="ceaea-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="ceaea-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="ceaea-185">Gibt die Telefoniefunktionen einer Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="ceaea-186">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="ceaea-187">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="ceaea-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="ceaea-188">Gibt den aktuellen Status einer angegebenen Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-188">Returns current status of a specified address.</span></span> <span data-ttu-id="ceaea-189">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="ceaea-190">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="ceaea-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="ceaea-191">Ruft die Anzahl der Adressbezeichner ab, die in der angegebenen Zeile unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ceaea-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="ceaea-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="ceaea-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="ceaea-193">Ruft die Adress-ID einer Adresse ab, die in einem alternativen Format angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ceaea-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="ceaea-194">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="ceaea-195">Öffnen und Schließen von Line-Geräten</span><span class="sxs-lookup"><span data-stu-id="ceaea-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="ceaea-196">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-196">Function</span></span>                                                         |   <span data-ttu-id="ceaea-197">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-198">**\_TSPI-ZeileOpen**</span><span class="sxs-lookup"><span data-stu-id="ceaea-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="ceaea-199">Öffnet ein angegebenes Liniengerät für die nachfolgende Überwachung und/oder Steuerung der Linie.</span><span class="sxs-lookup"><span data-stu-id="ceaea-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="ceaea-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-200">Synchronous.</span></span> |
| [<span data-ttu-id="ceaea-201">**\_TSPI-ZeileSchließen**</span><span class="sxs-lookup"><span data-stu-id="ceaea-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="ceaea-202">Schließt ein angegebenes geöffnetes Zeilengerät.</span><span class="sxs-lookup"><span data-stu-id="ceaea-202">Closes a specified opened line device.</span></span> <span data-ttu-id="ceaea-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="ceaea-204">Aufrufzustände und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ceaea-204">Call States and Events</span></span>



|  <span data-ttu-id="ceaea-205">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-205">Function</span></span>                                                         |   <span data-ttu-id="ceaea-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-207">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="ceaea-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="ceaea-208">Gibt feste Informationen zu einem Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-208">Returns fixed information about a call.</span></span> <span data-ttu-id="ceaea-209">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="ceaea-210">**\_TSPI-ZeileGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="ceaea-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="ceaea-211">Gibt vollständige Aufrufstatusinformationen für den angegebenen Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="ceaea-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-212">Synchronous.</span></span>       |
| [<span data-ttu-id="ceaea-213">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="ceaea-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="ceaea-214">Legt das anwendungsspezifische Feld der Informationsstruktur eines Aufrufs fest.</span><span class="sxs-lookup"><span data-stu-id="ceaea-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="ceaea-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ceaea-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="ceaea-216">Tätigen von Aufrufen</span><span class="sxs-lookup"><span data-stu-id="ceaea-216">Making Calls</span></span>



|  <span data-ttu-id="ceaea-217">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-217">Function</span></span>                                                         |   <span data-ttu-id="ceaea-218">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-219">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="ceaea-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="ceaea-220">Macht einen ausgehenden Aufruf und gibt ein Aufrufhand handle dafür zurück.</span><span class="sxs-lookup"><span data-stu-id="ceaea-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="ceaea-221">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="ceaea-221">Asynchronous.</span></span> |
| [<span data-ttu-id="ceaea-222">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="ceaea-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="ceaea-223">Wählt (Teile einer oder mehrere) wählbare Adressen.</span><span class="sxs-lookup"><span data-stu-id="ceaea-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="ceaea-224">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="ceaea-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="ceaea-225">Beantworten eingehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="ceaea-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="ceaea-226">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-226">Function</span></span>                                                         |   <span data-ttu-id="ceaea-227">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="ceaea-228">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="ceaea-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="ceaea-229">Beantwortet einen eingehenden Anruf.</span><span class="sxs-lookup"><span data-stu-id="ceaea-229">Answers an incoming call.</span></span> <span data-ttu-id="ceaea-230">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="ceaea-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="ceaea-231">Drop-Funktionen für Aufrufe</span><span class="sxs-lookup"><span data-stu-id="ceaea-231">Call Drop Functions</span></span>



|  <span data-ttu-id="ceaea-232">Funktion</span><span class="sxs-lookup"><span data-stu-id="ceaea-232">Function</span></span>                                                         |   <span data-ttu-id="ceaea-233">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceaea-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="ceaea-234">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="ceaea-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="ceaea-235">Trennt einen Aufruf oder verabsehrt einen aufrufversuch, der in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="ceaea-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="ceaea-236">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="ceaea-236">Asynchronous.</span></span> |



 

 

 
