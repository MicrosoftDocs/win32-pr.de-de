---
description: Dialogfeld "ChooseFont() Win32 Common"
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Dialogfeld "ChooseFont() Win32 Common"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088608"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="d97bb-103">Dialogfeld "ChooseFont() Win32 Common"</span><span class="sxs-lookup"><span data-stu-id="d97bb-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d97bb-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="d97bb-104">Affected Platforms</span></span>

<span data-ttu-id="d97bb-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="d97bb-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d97bb-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d97bb-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d97bb-107">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="d97bb-107">Feature Impact</span></span>

<span data-ttu-id="d97bb-108">**Schweregrad –** Niedrig</span><span class="sxs-lookup"><span data-stu-id="d97bb-108">**Severity** - Low</span></span>  
<span data-ttu-id="d97bb-109">**Häufigkeit** – Mittel</span><span class="sxs-lookup"><span data-stu-id="d97bb-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="d97bb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d97bb-110">Description</span></span>

<span data-ttu-id="d97bb-111">Windows 7 enthält mehrere Updates des allgemeinen Dialogfelds ChooseFont() Win32.</span><span class="sxs-lookup"><span data-stu-id="d97bb-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="d97bb-112">Diese lassen sich in zwei Kategorien unterteilen:</span><span class="sxs-lookup"><span data-stu-id="d97bb-112">These fall into two categories:</span></span>

-   <span data-ttu-id="d97bb-113">Visuelle Aktualisierung des Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="d97bb-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="d97bb-114">Unterstützung für neue Funktion zum Ein-/Ausblenden von Schriftarten</span><span class="sxs-lookup"><span data-stu-id="d97bb-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="d97bb-115">Die **Dialogaktualisierung** aktualisiert die Standardvorlage, um den Dialog stärker mit anderen Dialoglayouts in Windows in Einklang zu bringen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="d97bb-116">Es führt WYSIWYG in die Schriftartanzeigelisten ein, um Benutzern die Auswahl von Schriftarten zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="d97bb-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="d97bb-117">Es enthält auch einen Link zur Schriftarten-CPL, um Benutzern, die ihre Schriftartlisten anpassen möchten, einfachen Zugriff zu bieten.</span><span class="sxs-lookup"><span data-stu-id="d97bb-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="d97bb-118">**Schriftarten ein-/ausblenden** ist ein neues Windows 7-Plattformfeature, bei dem Schriftarten, die nicht für die Spracheinstellungen des aktuellen Benutzers geeignet sind (Eingabemethoden), nicht standardmäßig in Schriftartauswahllisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d97bb-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="d97bb-119">Benutzer können die Schriftarten anpassen, die in der Schriftarten-CPL angezeigt werden sollen, oder diese Funktion deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d97bb-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d97bb-120">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="d97bb-120">Manifestation of Impact</span></span>

<span data-ttu-id="d97bb-121">**Visuelle Aktualisierung des Dialogfelds**</span><span class="sxs-lookup"><span data-stu-id="d97bb-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="d97bb-122">Wir haben zwei neue Vorlagen in Windows 7 eingeführt (eine für Anwendungen, die Version 6 oder höher von comctl32.dll und eine für Anwendungen, die frühere Versionen laden).</span><span class="sxs-lookup"><span data-stu-id="d97bb-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="d97bb-123">Aus Gründen der Anwendungskompatibilität werden diese neuen Vorlagen nur für Anwendungen geladen, die nicht mit der ChooseFont-Nachrichtenwarteschlange in eine Warteschlange einhängen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="d97bb-124">Anwendungen, die die Nachrichtenwarteschlange einhängen, sehen weiterhin das alte Dialoglayout.</span><span class="sxs-lookup"><span data-stu-id="d97bb-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="d97bb-125">Anwendungen, die eigene Vorlagen bereitstellen, können sie weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="d97bb-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="d97bb-126">Anwendungen, die die neuen Vorlagen nicht erhalten, sehen keine Änderungen am Dialogfeldlayout von Vista.</span><span class="sxs-lookup"><span data-stu-id="d97bb-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="d97bb-127">Sie sollten jedoch weiterhin die neue WYSIWYG-Schriftartvorschau erhalten.</span><span class="sxs-lookup"><span data-stu-id="d97bb-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="d97bb-128">**Ein-/Ausblenden von Schriftarten**</span><span class="sxs-lookup"><span data-stu-id="d97bb-128">**Show/hide fonts**</span></span>

<span data-ttu-id="d97bb-129">Für alle Versionen von ChooseFont verwendet das Dialogfeld die Ein-/Ausblenden-Schriftarteinstellungen des aktuellen Benutzers, um die anzuzeigende Schriftartliste zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="d97bb-130">Dies führt dazu, dass in den meisten Instanzen weniger Schriftartlisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d97bb-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="d97bb-131">Entschärfung durch Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="d97bb-131">End-user Mitigation</span></span>

<span data-ttu-id="d97bb-132">**Schriftarten ein-/ausblenden:** Um das Ausblenden von Schriftarten zu deaktivieren, sollten Benutzer zur Seite Schriftarteinstellungen in der Schriftart-CPL wechseln und die Auswahl von aufheben.</span><span class="sxs-lookup"><span data-stu-id="d97bb-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="d97bb-133">Kontrollkästchen "Schriftarten basierend auf Spracheinstellungen ausblenden"</span><span class="sxs-lookup"><span data-stu-id="d97bb-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="d97bb-134">Entschärfung für Entwickler</span><span class="sxs-lookup"><span data-stu-id="d97bb-134">Developer Mitigation</span></span>

-   <span data-ttu-id="d97bb-135">**Visuelle Aktualisierung:** Anwendungsentwickler, die ihre eigenen Vorlagen bereitstellen, möchten diese möglicherweise aktualisieren, um mit der entsprechenden neuen Windows 7-Vorlage in Einklang zu stehen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="d97bb-136">Die neuen Vorlagen sind in der Vorlagendatei Font.dlg verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d97bb-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="d97bb-137">**Hinweis:** Die neue veröffentlichte Vorlage enthält ein zusätzliches SysLink-Steuerelement, das eine Verknüpfung bietet, mit der Benutzer die Schriftart-CPL starten können, um weitere Schriftarten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="d97bb-138">Für das Link-Steuerelement ist Version 6 der allgemeinen Windows-Steuerelementbibliothek (Common Control Library, comctl32.dll) comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="d97bb-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="d97bb-139">Entwickler sollten ein Manifest oder eine Direktive bereitstellen, das die Verwendung von Version 6 der DLL angibt, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d97bb-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="d97bb-140">Wenn eine Anwendung eine frühere Version der allgemeinen Steuerelementbibliothek verwendet, verwenden Sie stattdessen den Steuerelementtyp "PUSHBUTTON".</span><span class="sxs-lookup"><span data-stu-id="d97bb-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="d97bb-141">**Schriftarten ein-/ausblenden:** Entwickler können dieses Feature deaktivieren, indem sie ein zusätzliches Flag (CF \_ INACTIVEFONTS) im Flags-Member der CHOOSEFONT-Struktur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="d97bb-142">Wenn Sie dieses Flag festlegen, werden alle installierten Schriftarten in der Schriftartenliste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d97bb-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="d97bb-143">**Schriftarten ein-/ausblenden:** Anwendungen, die ChooseFont-Hilfeinhalte bereitstellen, möchten möglicherweise Inhalte hinzufügen, um zu erläutern, warum die Schriftartliste reduziert wird, und Benutzer an die Schriftarten-CPL leiten, um ihre Schriftartlisten anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d97bb-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="d97bb-144">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests</span><span class="sxs-lookup"><span data-stu-id="d97bb-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="d97bb-145">Entwickler, deren Anwendungen die ChooseFont-Nachrichtenwarteschlange verknüpfen, um das Dialogfeld anzupassen, sollten überprüfen, ob ihre Anwendungen alle vorhandenen Funktionen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d97bb-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="d97bb-146">Anwendungen, die die Schriftartliste mit Flags stark kürzen, sollten sicherstellen, dass die angezeigte Schriftartliste akzeptabel bleibt.</span><span class="sxs-lookup"><span data-stu-id="d97bb-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



