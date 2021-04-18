---
description: Mit dem PenInputPanel-Objekt können Sie Ihren Anwendungen problemlos direkte Stift Eingaben hinzufügen.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: "\"Pinputpanel\"-Klasse (\"msink AUT. h\")"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366227"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="a2086-103">Pinputpanel-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2086-103">PenInputPanel class</span></span>

<span data-ttu-id="a2086-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a2086-104">\[Deprecated.</span></span> <span data-ttu-id="a2086-105">" **Tzinputpanel** " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="a2086-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="a2086-106">Mit dem **PenInputPanel** -Objekt können Sie Ihren Anwendungen problemlos direkte Stift Eingaben hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2086-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="a2086-107">Das Objekt " **pinputpanel** " steht als anfügbares Objekt zur Verfügung, mit dem Sie vorhandenen Steuerelementen Tablet PC-Eingabe Bereichs Funktionen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="a2086-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="a2086-108">Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabe Sprache vorgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2086-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="a2086-109">Sie haben die Möglichkeit, die Standardeingabe Methode für **das Objekt "** " mit dem Objekt "", entweder Handschrift oder Tastatur, auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a2086-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="a2086-110">Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.</span><span class="sxs-lookup"><span data-stu-id="a2086-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="a2086-111">" **Pinputpanel** " verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a2086-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="a2086-112">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a2086-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="a2086-113">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a2086-113">Events</span></span>](#events)
-   [<span data-ttu-id="a2086-114">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a2086-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="a2086-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="a2086-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="a2086-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2086-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="a2086-117">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a2086-117">Enumerations</span></span>

<span data-ttu-id="a2086-118">Diese Enumerationen sind **in der Klasse** "" der Klasse "" von "".</span><span class="sxs-lookup"><span data-stu-id="a2086-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="a2086-119">Enumeration</span><span class="sxs-lookup"><span data-stu-id="a2086-119">Enumeration</span></span>                    | <span data-ttu-id="a2086-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2086-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2086-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="a2086-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="a2086-122">Definiert den Typ der Eingabe, die zurzeit im Objekt " **pinputpanel** " verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a2086-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="a2086-123">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a2086-123">Events</span></span>

<span data-ttu-id="a2086-124">Diese Ereignisse werden **von der Klasse** "" in der Klasse "".</span><span class="sxs-lookup"><span data-stu-id="a2086-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="a2086-125">Ereignis</span><span class="sxs-lookup"><span data-stu-id="a2086-125">Event</span></span>                                                  | <span data-ttu-id="a2086-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2086-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2086-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="a2086-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="a2086-128">Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt " **pinputpanel** " Benutzereingaben in das angefügte Steuerelement einfügen konnte.</span><span class="sxs-lookup"><span data-stu-id="a2086-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="a2086-129">**PanelChanged**</span><span class="sxs-lookup"><span data-stu-id="a2086-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="a2086-130">Tritt auf, wenn sich das Objekt " **pinputpanel** " zwischen Layouts ändert.</span><span class="sxs-lookup"><span data-stu-id="a2086-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="a2086-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="a2086-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="a2086-132">Tritt auf, wenn das Objekt " **pinputpanel** " verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a2086-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="a2086-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="a2086-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="a2086-134">Tritt auf, **Wenn das "** "-Objekt des ""-Objekts angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2086-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="a2086-135">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a2086-135">Interfaces</span></span>

<span data-ttu-id="a2086-136">Diese Schnittstellen werden von der Klasse " **pinputpanel** " definiert.</span><span class="sxs-lookup"><span data-stu-id="a2086-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="a2086-137">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a2086-137">Interface</span></span>          | <span data-ttu-id="a2086-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2086-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="a2086-139">**Ipinputpanel**</span><span class="sxs-lookup"><span data-stu-id="a2086-139">**IPenInputPanel**</span></span> | <span data-ttu-id="a2086-140">Dieses Objekt implementiert die **ipinputpanel** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a2086-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="a2086-141">Methoden</span><span class="sxs-lookup"><span data-stu-id="a2086-141">Methods</span></span>

<span data-ttu-id="a2086-142">Die Klasse " **pinputpanel** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a2086-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="a2086-143">Methode</span><span class="sxs-lookup"><span data-stu-id="a2086-143">Method</span></span>                                                         | <span data-ttu-id="a2086-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2086-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2086-145">**Commitpdinginput**</span><span class="sxs-lookup"><span data-stu-id="a2086-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="a2086-146">Sendet gesammelte frei Hand Eingaben an die Erkennung und stellt das Erkennungs Ergebnis dar.</span><span class="sxs-lookup"><span data-stu-id="a2086-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="a2086-147">**Enabletsf**</span><span class="sxs-lookup"><span data-stu-id="a2086-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="a2086-148">Wenn **true** angegeben wird, versucht das " **tzinputpanel** ", Text über das Text Services-Framework (TSF) an das angefügte Steuerelement zu senden, und ermöglicht die Verwendung der Benutzeroberfläche zur Korrektur.</span><span class="sxs-lookup"><span data-stu-id="a2086-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="a2086-149">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="a2086-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="a2086-150">Legt die Position des " **pinputpanel** "-Objekts auf eine statische Bildschirmposition fest.</span><span class="sxs-lookup"><span data-stu-id="a2086-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="a2086-151">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="a2086-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="a2086-152">Aktualisiert und stellt die **PenInputPanel** -Eigenschaften auf Grundlage der Einstellungen für den Tablet PC-Eingabebereich wieder her, positioniert automatisch den Stift Eingabebereich und legt die Benutzeroberfläche auf den Standardbereich fest.</span><span class="sxs-lookup"><span data-stu-id="a2086-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a2086-153">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2086-153">Properties</span></span>

<span data-ttu-id="a2086-154">Die Klasse " **pinputpanel** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2086-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="a2086-155">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2086-155">Property</span></span>                                                                  | <span data-ttu-id="a2086-156">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a2086-156">Access type</span></span>           | <span data-ttu-id="a2086-157">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2086-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2086-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="a2086-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="a2086-159">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-159">Read/write</span></span><br/> | <span data-ttu-id="a2086-160">Ruft das Fenster Handle des Steuer Elements ab oder legt dieses fest, an das das " **pinputpanel** "-Objekt angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a2086-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="a2086-161">**Automatisch anzeigen**</span><span class="sxs-lookup"><span data-stu-id="a2086-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="a2086-162">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-162">Read/write</span></span><br/> | <span data-ttu-id="a2086-163">Ruft einen booleschen Wert ab, der angibt, ob das **PenInputPanel** -Objekt angezeigt wird, wenn der Fokus mithilfe des Stifts festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="a2086-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="a2086-164">**Busy**</span><span class="sxs-lookup"><span data-stu-id="a2086-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="a2086-165">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2086-165">Read-only</span></span><br/>  | <span data-ttu-id="a2086-166">Ruft einen booleschen Wert ab, der angibt, ob das " **cuinputpanel** "-Objekt zurzeit frei Hand Eingaben verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a2086-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="a2086-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="a2086-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="a2086-168">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-168">Read/write</span></span><br/> | <span data-ttu-id="a2086-169">Ruft ab oder legt fest, welcher Panel-Typ zurzeit für Eingaben innerhalb des " **pinputpanel** "-Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2086-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="a2086-170">**Defaultpanel**</span><span class="sxs-lookup"><span data-stu-id="a2086-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="a2086-171">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-171">Read/write</span></span><br/> | <span data-ttu-id="a2086-172">Ruft ab oder legt fest, welcher Bereichs Datentyp der Standard Bereichs Datentyp ist **, der für** die Eingabe innerhalb des "" "" "" "</span><span class="sxs-lookup"><span data-stu-id="a2086-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="a2086-173">**Faktoid**</span><span class="sxs-lookup"><span data-stu-id="a2086-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="a2086-174">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-174">Read/write</span></span><br/> | <span data-ttu-id="a2086-175">Ruft den Zeichen folgen Namen des in der Erkennung verwendeten Faktoid ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a2086-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="a2086-176">**Höhe**</span><span class="sxs-lookup"><span data-stu-id="a2086-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="a2086-177">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2086-177">Read-only</span></span><br/>  | <span data-ttu-id="a2086-178">Ruft die Höhe des " **pinputpanel** "-Objekts in Client Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="a2086-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a2086-179">**Horizontal Offset**</span><span class="sxs-lookup"><span data-stu-id="a2086-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="a2086-180">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-180">Read/write</span></span><br/> | <span data-ttu-id="a2086-181">Ruft den Offset zwischen dem linken Rand des " **pinputpanel** "-Objekts und dem linken Rand des Steuer Elements ab, an das es angefügt ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a2086-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="a2086-182">**Linken**</span><span class="sxs-lookup"><span data-stu-id="a2086-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="a2086-183">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2086-183">Read-only</span></span><br/>  | <span data-ttu-id="a2086-184">Ruft die horizontale bzw. x-Achse, Position des linken Rands des " **tabinputpanel** "-Objekts in Bildschirm Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="a2086-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="a2086-185">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="a2086-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="a2086-186">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2086-186">Read-only</span></span><br/>  | <span data-ttu-id="a2086-187">Ruft die vertikale Achse bzw. y-Achse, Position des oberen Rands des **Objekt-** Objekts in Bildschirm Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="a2086-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="a2086-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="a2086-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="a2086-189">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-189">Read/write</span></span><br/> | <span data-ttu-id="a2086-190">Ruft den Offset zwischen dem nächstgelegenen horizontalen Rand des " **kinputpanel** "-Objekts und dem nächstgelegenen horizontalen Rand des Steuer Elements ab, an das es angefügt ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a2086-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="a2086-191">**Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="a2086-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="a2086-192">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a2086-192">Read/write</span></span><br/> | <span data-ttu-id="a2086-193">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das Objekt " **pinput Panel** " sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="a2086-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="a2086-194">**Breite**</span><span class="sxs-lookup"><span data-stu-id="a2086-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="a2086-195">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a2086-195">Read-only</span></span><br/>  | <span data-ttu-id="a2086-196">Ruft die Breite des " **pinputpanel** "-Objekts in Client Koordinaten ab.</span><span class="sxs-lookup"><span data-stu-id="a2086-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="a2086-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2086-197">Remarks</span></span>

<span data-ttu-id="a2086-198">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2086-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2086-199">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2086-199">Requirements</span></span>



| <span data-ttu-id="a2086-200">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2086-200">Requirement</span></span> | <span data-ttu-id="a2086-201">Wert</span><span class="sxs-lookup"><span data-stu-id="a2086-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2086-202">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2086-202">Minimum supported client</span></span><br/> | <span data-ttu-id="a2086-203">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2086-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a2086-204">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2086-204">Minimum supported server</span></span><br/> | <span data-ttu-id="a2086-205">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a2086-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a2086-206">Header</span><span class="sxs-lookup"><span data-stu-id="a2086-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2086-207"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2086-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2086-208">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2086-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2086-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2086-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a2086-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2086-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2086-211">Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"</span><span class="sxs-lookup"><span data-stu-id="a2086-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
