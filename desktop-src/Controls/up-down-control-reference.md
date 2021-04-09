---
title: Up-Down-Steuerelement
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit auf-ab-Steuerelementen verwendet werden.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036799"
---
# <a name="up-down-control"></a><span data-ttu-id="116ec-103">Up-Down-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="116ec-103">Up-Down Control</span></span>

<span data-ttu-id="116ec-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit auf-ab-Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="116ec-104">This section contains information about the programming elements used with up-down controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="116ec-105">Übersichten</span><span class="sxs-lookup"><span data-stu-id="116ec-105">Overviews</span></span>



| <span data-ttu-id="116ec-106">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-106">Topic</span></span>                                    | <span data-ttu-id="116ec-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-107">Contents</span></span>                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-108">Auf-ab-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="116ec-108">Up-Down Controls</span></span>](up-down-controls.md) | <span data-ttu-id="116ec-109">Ein auf-ab-Steuerelement ist ein paar von Pfeil Schaltflächen, auf die der Benutzer klicken kann, um einen Wert zu erhöhen oder zu verringern, z. b. eine Bild Lauf Position oder eine Zahl, die in einem Begleit Steuerelement (einem Buddy-Fenster) angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="116ec-109">An up-down control is a pair of arrow buttons that the user can click to increment or decrement a value, such as a scroll position or a number displayed in a companion control (called a buddy window).</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="116ec-110">Functions</span><span class="sxs-lookup"><span data-stu-id="116ec-110">Functions</span></span>



| <span data-ttu-id="116ec-111">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-111">Topic</span></span>                                              | <span data-ttu-id="116ec-112">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-112">Contents</span></span>                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-113">**"Kreateupdowncontrol"**</span><span class="sxs-lookup"><span data-stu-id="116ec-113">**CreateUpDownControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | <span data-ttu-id="116ec-114">Erstellt ein auf-ab-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="116ec-114">Creates an up-down control.</span></span> <span data-ttu-id="116ec-115">Hinweis: Diese Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="116ec-115">Note: This function is obsolete.</span></span> <span data-ttu-id="116ec-116">Es handelt sich um eine 16-Bit-Funktion und kann keine 32-Bit-Werte für Bereich und Position verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="116ec-116">It is a 16 bit function and cannot handle 32 bit values for range and position.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="116ec-117">Meldungen</span><span class="sxs-lookup"><span data-stu-id="116ec-117">Messages</span></span>



| <span data-ttu-id="116ec-118">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-118">Topic</span></span>                                                 | <span data-ttu-id="116ec-119">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-119">Contents</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-120">**UDM \_ GetAccel**</span><span class="sxs-lookup"><span data-stu-id="116ec-120">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)                 | <span data-ttu-id="116ec-121">Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-121">Retrieves acceleration information for an up-down control.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="116ec-122">**UDM \_ GetBase**</span><span class="sxs-lookup"><span data-stu-id="116ec-122">**UDM\_GETBASE**</span></span>](udm-getbase.md)                   | <span data-ttu-id="116ec-123">Ruft die aktuelle Basis 10 (d. h. entweder Basis 10 oder 16) für ein auf-ab-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-123">Retrieves the current radix base (that is, either base 10 or 16) for an up-down control.</span></span> <br/>                                                                                                                                   |
| [<span data-ttu-id="116ec-124">**UDM \_ GetBuddy**</span><span class="sxs-lookup"><span data-stu-id="116ec-124">**UDM\_GETBUDDY**</span></span>](udm-getbuddy.md)                 | <span data-ttu-id="116ec-125">Ruft das Handle für das aktuelle Buddy-Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-125">Retrieves the handle to the current buddy window.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="116ec-126">**UDM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="116ec-126">**UDM\_GETPOS**</span></span>](udm-getpos.md)                     | <span data-ttu-id="116ec-127">Ruft die aktuelle Position eines auf-ab-Steuer Elements mit 16-Bit-Genauigkeit ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-127">Retrieves the current position of an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="116ec-128">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="116ec-128">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)                 | <span data-ttu-id="116ec-129">Gibt die 32-Bit-Position eines auf-ab-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="116ec-129">Returns the 32-bit position of an up-down control.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="116ec-130">**UDM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="116ec-130">**UDM\_GETRANGE**</span></span>](udm-getrange.md)                 | <span data-ttu-id="116ec-131">Ruft die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-131">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="116ec-132">**UDM \_ GETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="116ec-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)             | <span data-ttu-id="116ec-133">Ruft den 32-Bit-Bereich eines auf-ab-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-133">Retrieves the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                          |
| [<span data-ttu-id="116ec-134">**UDM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="116ec-134">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md) | <span data-ttu-id="116ec-135">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="116ec-135">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                                                               |
| [<span data-ttu-id="116ec-136">**UDM- \_ SetAccel**</span><span class="sxs-lookup"><span data-stu-id="116ec-136">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)                 | <span data-ttu-id="116ec-137">Legt die Beschleunigung für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-137">Sets the acceleration for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="116ec-138">**UDM- \_ setbase**</span><span class="sxs-lookup"><span data-stu-id="116ec-138">**UDM\_SETBASE**</span></span>](udm-setbase.md)                   | <span data-ttu-id="116ec-139">Legt die Basis für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-139">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="116ec-140">Der Basiswert bestimmt, ob das Buddy-Fenster Zahlen in Dezimal-oder hexadezimal Ziffern anzeigt.</span><span class="sxs-lookup"><span data-stu-id="116ec-140">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="116ec-141">Hexadezimale Zahlen sind immer unsigniert, und Dezimalzahlen werden signiert.</span><span class="sxs-lookup"><span data-stu-id="116ec-141">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span> <br/> |
| [<span data-ttu-id="116ec-142">**UDM- \_ SetBuddy**</span><span class="sxs-lookup"><span data-stu-id="116ec-142">**UDM\_SETBUDDY**</span></span>](udm-setbuddy.md)                 | <span data-ttu-id="116ec-143">Legt das Buddy-Fenster für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-143">Sets the buddy window for an up-down control.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="116ec-144">**UDM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="116ec-144">**UDM\_SETPOS**</span></span>](udm-setpos.md)                     | <span data-ttu-id="116ec-145">Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-145">Sets the current position for an up-down control with 16-bit precision.</span></span> <br/>                                                                                                                                                    |
| [<span data-ttu-id="116ec-146">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="116ec-146">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)                 | <span data-ttu-id="116ec-147">Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-147">Sets the position of an up-down control with 32-bit precision.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="116ec-148">**UDM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="116ec-148">**UDM\_SETRANGE**</span></span>](udm-setrange.md)                 | <span data-ttu-id="116ec-149">Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-149">Sets the minimum and maximum positions (range) for an up-down control.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="116ec-150">**UDM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="116ec-150">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)             | <span data-ttu-id="116ec-151">Legt den 32-Bit-Bereich eines auf-ab-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-151">Sets the 32-bit range of an up-down control.</span></span> <br/>                                                                                                                                                                               |
| [<span data-ttu-id="116ec-152">**UDM- \_ Format-Code Format**</span><span class="sxs-lookup"><span data-stu-id="116ec-152">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md) | <span data-ttu-id="116ec-153">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="116ec-153">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="116ec-154">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="116ec-154">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/>                                   |



 

### <a name="notifications"></a><span data-ttu-id="116ec-155">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="116ec-155">Notifications</span></span>



| <span data-ttu-id="116ec-156">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-156">Topic</span></span>                                                            | <span data-ttu-id="116ec-157">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-157">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-158">NM \_ releasedcapture (auf-ab)</span><span class="sxs-lookup"><span data-stu-id="116ec-158">NM\_RELEASEDCAPTURE (up-down)</span></span>](nm-releasedcapture-up-down-.md) | <span data-ttu-id="116ec-159">Benachrichtigt das übergeordnete Fenster eines auf-ab-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt.</span><span class="sxs-lookup"><span data-stu-id="116ec-159">Notifies an up-down control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="116ec-160">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="116ec-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                                                                                                                                       |
| [<span data-ttu-id="116ec-161">udn-Delta Torys \_</span><span class="sxs-lookup"><span data-stu-id="116ec-161">UDN\_DELTAPOS</span></span>](udn-deltapos.md)                                | <span data-ttu-id="116ec-162">Wird vom Betriebssystem an das übergeordnete Fenster eines auf-ab-Steuer Elements gesendet, wenn sich die Position des-Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="116ec-162">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="116ec-163">Dies geschieht, wenn der Benutzer eine Änderung des Werts anfordert, indem er den Pfeil nach oben oder nach unten drückt.</span><span class="sxs-lookup"><span data-stu-id="116ec-163">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="116ec-164">Die [udn- \_ Delta](udn-deltapos.md) -Nachricht wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="116ec-164">The [UDN\_DELTAPOS](udn-deltapos.md) message is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="116ec-165">Strukturen</span><span class="sxs-lookup"><span data-stu-id="116ec-165">Structures</span></span>



| <span data-ttu-id="116ec-166">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-166">Topic</span></span>                        | <span data-ttu-id="116ec-167">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-167">Contents</span></span>                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-168">**Nmupdown**</span><span class="sxs-lookup"><span data-stu-id="116ec-168">**NMUPDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | <span data-ttu-id="116ec-169">Enthält Informationen, die spezifisch für die Benachrichtigungs Meldungen auf der auf-ab-</span><span class="sxs-lookup"><span data-stu-id="116ec-169">Contains information specific to up-down control notification messages.</span></span> <span data-ttu-id="116ec-170">Sie ist identisch mit und ersetzt die **- \_ UpDown** -Struktur von nm.</span><span class="sxs-lookup"><span data-stu-id="116ec-170">It is identical to and replaces the **NM\_UPDOWN** structure.</span></span> <br/> |
| [<span data-ttu-id="116ec-171">**Udaccel**</span><span class="sxs-lookup"><span data-stu-id="116ec-171">**UDACCEL**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | <span data-ttu-id="116ec-172">Enthält Beschleunigungs Informationen für ein auf-ab-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="116ec-172">Contains acceleration information for an up-down control.</span></span> <br/>                                                                             |



 

### <a name="constants"></a><span data-ttu-id="116ec-173">Konstanten</span><span class="sxs-lookup"><span data-stu-id="116ec-173">Constants</span></span>



| <span data-ttu-id="116ec-174">Thema</span><span class="sxs-lookup"><span data-stu-id="116ec-174">Topic</span></span>                                                | <span data-ttu-id="116ec-175">Inhalte</span><span class="sxs-lookup"><span data-stu-id="116ec-175">Contents</span></span>                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="116ec-176">Auf-ab-Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="116ec-176">Up-Down Control Styles</span></span>](up-down-control-styles.md) | <span data-ttu-id="116ec-177">In diesem Abschnitt werden die Formate aufgelistet, die bei der Erstellung von auf-ab-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="116ec-177">This section lists the styles used when creating up-down controls.</span></span><br/> |



 

 

 





