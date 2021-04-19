---
description: Die zusätzlichen Telefondienst Funktionen sind in den folgenden Themen nach Kategorie aufgelistet.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Zusätzliche Funktionen für den Telefondienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367931"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="7e53c-103">Zusätzliche Funktionen für den Telefondienst</span><span class="sxs-lookup"><span data-stu-id="7e53c-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="7e53c-104">Die zusätzlichen Telefondienst Funktionen sind in den folgenden Themen nach Kategorie aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7e53c-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="7e53c-105">Eine Funktion wird als [*asynchron*](a-tapgloss.md) identifiziert, wenn Sie die Vervollständigung in einer Antwortmeldung an die Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="7e53c-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="7e53c-106">Wenn die Funktion das Ergebnis immer sofort an die Anwendung zurückgibt, gilt die Funktion als [*synchron*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="7e53c-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="7e53c-107">Im folgenden finden Sie eine funktionale Gruppierung der ergänzenden Phone Service-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="7e53c-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="7e53c-108">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="7e53c-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="7e53c-109">Datenbereiche</span><span class="sxs-lookup"><span data-stu-id="7e53c-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="7e53c-110">Anzeige</span><span class="sxs-lookup"><span data-stu-id="7e53c-110">Display</span></span>](#display)
-   [<span data-ttu-id="7e53c-111">Gerätewechsel Geräte</span><span class="sxs-lookup"><span data-stu-id="7e53c-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="7e53c-112">Aufleuchten</span><span class="sxs-lookup"><span data-stu-id="7e53c-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="7e53c-113">Öffnen und Schließen von Telefongeräten</span><span class="sxs-lookup"><span data-stu-id="7e53c-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="7e53c-114">Telefon Initialisierung und Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="7e53c-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="7e53c-115">Telefonstatus und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e53c-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="7e53c-116">Aushandlung der Telefon Version</span><span class="sxs-lookup"><span data-stu-id="7e53c-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="7e53c-117">Mandel</span><span class="sxs-lookup"><span data-stu-id="7e53c-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="7e53c-118">Status</span><span class="sxs-lookup"><span data-stu-id="7e53c-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="7e53c-119">Telefon Initialisierung und Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="7e53c-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="7e53c-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-120">Function</span></span>                                       | <span data-ttu-id="7e53c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-122">**phoneinitializeex**</span><span class="sxs-lookup"><span data-stu-id="7e53c-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="7e53c-123">Initialisiert die TAPI-telefonabstraktion zur Verwendung durch die Aufruf Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7e53c-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="7e53c-124">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-124">Synchronous.</span></span> |
| [<span data-ttu-id="7e53c-125">**phoneshutdown**</span><span class="sxs-lookup"><span data-stu-id="7e53c-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="7e53c-126">Fährt die Verwendung der TAPI-Telefon Abstraktion für eine Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="7e53c-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="7e53c-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="7e53c-128">Aushandlung der Telefon Version</span><span class="sxs-lookup"><span data-stu-id="7e53c-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="7e53c-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-129">Function</span></span>                                                     | <span data-ttu-id="7e53c-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-131">**phonenegotiateapiversion**</span><span class="sxs-lookup"><span data-stu-id="7e53c-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="7e53c-132">Ermöglicht es einer Anwendung, eine TAPI-Version für die Verwendung von auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="7e53c-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="7e53c-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="7e53c-134">Öffnen und Schließen von Telefongeräten</span><span class="sxs-lookup"><span data-stu-id="7e53c-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="7e53c-135">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-135">Function</span></span>                         | <span data-ttu-id="7e53c-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-137">**phoneopen**</span><span class="sxs-lookup"><span data-stu-id="7e53c-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="7e53c-138">Öffnet das angegebene Telefongerät und erteilt der Anwendung entweder Besitzer-oder Monitor Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="7e53c-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="7e53c-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-139">Synchronous.</span></span> |
| [<span data-ttu-id="7e53c-140">**phoneclose**</span><span class="sxs-lookup"><span data-stu-id="7e53c-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="7e53c-141">Schließt ein angegebenes geöffnetes Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="7e53c-141">Closes a specified open phone device.</span></span> <span data-ttu-id="7e53c-142">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="7e53c-143">Telefon Status und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e53c-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="7e53c-144">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-144">Function</span></span>                                       | <span data-ttu-id="7e53c-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-146">**phonegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="7e53c-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="7e53c-147">Gibt die Funktionen eines angegebenen Telefon Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="7e53c-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="7e53c-149">**phonegetid**</span><span class="sxs-lookup"><span data-stu-id="7e53c-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="7e53c-150">Gibt eine Geräte-ID für die angegebene Geräteklasse zurück, die dem angegebenen Telefongerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7e53c-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="7e53c-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="7e53c-152">**phonegeticon**</span><span class="sxs-lookup"><span data-stu-id="7e53c-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="7e53c-153">Ermöglicht es einer Anwendung, ein Symbol für die Anzeige für den Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e53c-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="7e53c-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="7e53c-155">**phoneconfigdialog**</span><span class="sxs-lookup"><span data-stu-id="7e53c-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="7e53c-156">Bewirkt, dass der Anbieter des angegebenen Telefon Geräts ein Dialogfeld anzeigt, das es dem Benutzer ermöglicht, Parameter im Zusammenhang mit dem Telefongerät zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7e53c-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="7e53c-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="7e53c-158">Gerätewechsel Geräte</span><span class="sxs-lookup"><span data-stu-id="7e53c-158">Hookswitch Devices</span></span>



| <span data-ttu-id="7e53c-159">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-159">Function</span></span>                                         | <span data-ttu-id="7e53c-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-161">**phonesethookswitch**</span><span class="sxs-lookup"><span data-stu-id="7e53c-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="7e53c-162">Legt den Hook-Zustand der geöffnenden Geräte eines geöffneten Telefons auf einen angegebenen Modus fest.</span><span class="sxs-lookup"><span data-stu-id="7e53c-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="7e53c-163">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="7e53c-164">**phonegethookswitch**</span><span class="sxs-lookup"><span data-stu-id="7e53c-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="7e53c-165">Fragt den Modus "geokswitch" eines geöffnenden Telefon Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7e53c-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="7e53c-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-166">Synchronous.</span></span>          |
| [<span data-ttu-id="7e53c-167">**phonesetvolume**</span><span class="sxs-lookup"><span data-stu-id="7e53c-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="7e53c-168">Legt das Volume eines geöffnenden Telefon Geräts für einen Hostgerät fest.</span><span class="sxs-lookup"><span data-stu-id="7e53c-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="7e53c-169">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="7e53c-170">**phonegetvolume**</span><span class="sxs-lookup"><span data-stu-id="7e53c-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="7e53c-171">Gibt die volumeeinstellung eines Sprechers eines geöffnenden Telefons für ein geöffnetes Telefongerät zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="7e53c-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-172">Synchronous.</span></span> |
| [<span data-ttu-id="7e53c-173">**phonesetgewinn**</span><span class="sxs-lookup"><span data-stu-id="7e53c-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="7e53c-174">Legt den Gewinn der MIC eines geöffnenden Telefon Geräts für ein geöffnetes Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="7e53c-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="7e53c-175">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="7e53c-176">**phonegetgewinn**</span><span class="sxs-lookup"><span data-stu-id="7e53c-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="7e53c-177">Gibt die ergriffseinstellung eines geöffnenden Telefons eines geöffnenden Telefons für ein geöffnetes Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="7e53c-178">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="7e53c-179">Anzeige</span><span class="sxs-lookup"><span data-stu-id="7e53c-179">Display</span></span>



| <span data-ttu-id="7e53c-180">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-180">Function</span></span>                                   | <span data-ttu-id="7e53c-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-182">**phonesetdisplay**</span><span class="sxs-lookup"><span data-stu-id="7e53c-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="7e53c-183">Schreibt Informationen in die Anzeige eines geöffneten Telefon Geräts.</span><span class="sxs-lookup"><span data-stu-id="7e53c-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="7e53c-184">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-184">Asynchronous.</span></span> |
| [<span data-ttu-id="7e53c-185">**phonegetdisplay**</span><span class="sxs-lookup"><span data-stu-id="7e53c-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="7e53c-186">Gibt den aktuellen Inhalt der Anzeige eines Telefons zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="7e53c-187">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="7e53c-188">Ring</span><span class="sxs-lookup"><span data-stu-id="7e53c-188">Ring</span></span>



| <span data-ttu-id="7e53c-189">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-189">Function</span></span>                             | <span data-ttu-id="7e53c-190">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-191">**phonesetring**</span><span class="sxs-lookup"><span data-stu-id="7e53c-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="7e53c-192">Beendet ein geöffnetes Telefongerät entsprechend einem bestimmten Ring Modus.</span><span class="sxs-lookup"><span data-stu-id="7e53c-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="7e53c-193">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-193">Asynchronous.</span></span> |
| [<span data-ttu-id="7e53c-194">**phonegetralling**</span><span class="sxs-lookup"><span data-stu-id="7e53c-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="7e53c-195">Gibt den aktuellen Ring Modus eines geöffneten Telefon Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="7e53c-196">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="7e53c-197">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="7e53c-197">Buttons</span></span>



| <span data-ttu-id="7e53c-198">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-198">Function</span></span>                                         | <span data-ttu-id="7e53c-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-200">**phonesetbuttoninfo**</span><span class="sxs-lookup"><span data-stu-id="7e53c-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="7e53c-201">Legt die mit einer Schaltfläche auf einem Telefongerät verknüpften Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="7e53c-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="7e53c-202">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-202">Asynchronous.</span></span> |
| [<span data-ttu-id="7e53c-203">**phonegetbuttoninfo**</span><span class="sxs-lookup"><span data-stu-id="7e53c-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="7e53c-204">Gibt Informationen zurück, die mit einer Schaltfläche auf einem Telefongerät verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7e53c-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="7e53c-205">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="7e53c-206">Aufleuchten</span><span class="sxs-lookup"><span data-stu-id="7e53c-206">Lamps</span></span>



| <span data-ttu-id="7e53c-207">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-207">Function</span></span>                             | <span data-ttu-id="7e53c-208">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-209">**phonesetlamp**</span><span class="sxs-lookup"><span data-stu-id="7e53c-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="7e53c-210">Leuchtet eine LAMP auf einem angegebenen geöffneten Telefongerät in einem bestimmten Lamp-Beleuchtungs Modus.</span><span class="sxs-lookup"><span data-stu-id="7e53c-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="7e53c-211">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-211">Asynchronous.</span></span> |
| [<span data-ttu-id="7e53c-212">**phonegetlamp**</span><span class="sxs-lookup"><span data-stu-id="7e53c-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="7e53c-213">Gibt den aktuellen Lamp-Modus der angegebenen Lamp zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="7e53c-214">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="7e53c-215">Datenbereiche</span><span class="sxs-lookup"><span data-stu-id="7e53c-215">Data Areas</span></span>



| <span data-ttu-id="7e53c-216">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-216">Function</span></span>                             | <span data-ttu-id="7e53c-217">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-218">**phonesetdata**</span><span class="sxs-lookup"><span data-stu-id="7e53c-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="7e53c-219">Lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter.</span><span class="sxs-lookup"><span data-stu-id="7e53c-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="7e53c-220">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="7e53c-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="7e53c-221">**phonegetdata**</span><span class="sxs-lookup"><span data-stu-id="7e53c-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="7e53c-222">Lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch.</span><span class="sxs-lookup"><span data-stu-id="7e53c-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="7e53c-223">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="7e53c-224">Status</span><span class="sxs-lookup"><span data-stu-id="7e53c-224">Status</span></span>



| <span data-ttu-id="7e53c-225">Funktion</span><span class="sxs-lookup"><span data-stu-id="7e53c-225">Function</span></span>                                                 | <span data-ttu-id="7e53c-226">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e53c-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e53c-227">**phonesetstatus-Meldungen**</span><span class="sxs-lookup"><span data-stu-id="7e53c-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="7e53c-228">Gibt die Statusänderungen an, für die die Anwendung benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e53c-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="7e53c-229">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-229">Synchronous.</span></span> |
| [<span data-ttu-id="7e53c-230">**phonegetstatus Messages**</span><span class="sxs-lookup"><span data-stu-id="7e53c-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="7e53c-231">Gibt die Statusänderungen zurück, für die die Anwendung benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e53c-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="7e53c-232">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-232">Synchronous.</span></span>   |
| [<span data-ttu-id="7e53c-233">**phonegetstatus**</span><span class="sxs-lookup"><span data-stu-id="7e53c-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="7e53c-234">Gibt den gesamten Status eines geöffneten Telefon Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="7e53c-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="7e53c-235">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="7e53c-235">Synchronous.</span></span>                         |



 

 

 



