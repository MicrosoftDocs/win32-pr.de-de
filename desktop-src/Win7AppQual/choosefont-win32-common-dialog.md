---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Ausgewählter Win32-Dialog Feld ()
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352760"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="39b4f-103">Ausgewählter Win32-Dialog Feld ()</span><span class="sxs-lookup"><span data-stu-id="39b4f-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="39b4f-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="39b4f-104">Affected Platforms</span></span>

<span data-ttu-id="39b4f-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="39b4f-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="39b4f-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39b4f-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="39b4f-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="39b4f-107">Feature Impact</span></span>

<span data-ttu-id="39b4f-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="39b4f-108">**Severity** - Low</span></span>  
<span data-ttu-id="39b4f-109">**Frequency** -Medium</span><span class="sxs-lookup"><span data-stu-id="39b4f-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="39b4f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39b4f-110">Description</span></span>

<span data-ttu-id="39b4f-111">Windows 7 enthält mehrere Updates für das allgemeine Win32-Dialogfeld ().</span><span class="sxs-lookup"><span data-stu-id="39b4f-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="39b4f-112">Diese werden in zwei Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="39b4f-112">These fall into two categories:</span></span>

-   <span data-ttu-id="39b4f-113">Visuelle Aktualisierung des Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="39b4f-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="39b4f-114">Unterstützung für neue Funktionen zum Anzeigen/Ausblenden von Schriftarten</span><span class="sxs-lookup"><span data-stu-id="39b4f-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="39b4f-115">Die **Dialogfeld Aktualisierung** aktualisiert die Standardvorlage, damit das Dialogfeld mit anderen Dialog Layouts in Windows in Einklang gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="39b4f-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="39b4f-116">Es führt WYSIWYG in die Schriftart Anzeigelisten ein, um Benutzern die Auswahl von Schriftarten zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="39b4f-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="39b4f-117">Außerdem ist ein Link zu den Schriftarten cpl enthalten, um Benutzern, die Ihre Schriftart Listen anpassen möchten, einen einfachen Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="39b4f-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="39b4f-118">**Schriftarten anzeigen/ausblenden** ist ein neues Feature für die Windows 7-Plattform, bei dem Schriftarten, die nicht für die Spracheinstellungen des aktuellen Benutzers geeignet sind (Eingabemethoden) standardmäßig nicht in den Schriftart Auswahllisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39b4f-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="39b4f-119">Benutzer können die Schriftarten anpassen, die in der Schriftarten-cpl angezeigt werden sollen, oder Sie können diese Funktion deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="39b4f-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="39b4f-120">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="39b4f-120">Manifestation of Impact</span></span>

<span data-ttu-id="39b4f-121">**Visuelle Aktualisierung des Dialog Felds**</span><span class="sxs-lookup"><span data-stu-id="39b4f-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="39b4f-122">Wir haben zwei neue Vorlagen in Windows 7 eingeführt (eine für Anwendungen, die Version 6 oder höher von comctl32.dll laden, und eine andere für Anwendungen, die frühere Versionen laden).</span><span class="sxs-lookup"><span data-stu-id="39b4f-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="39b4f-123">Aus Gründen der Anwendungs Kompatibilität werden diese neuen Vorlagen nur für Anwendungen geladen, die nicht mit der Nachrichten Warteschlange "choosefont" kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="39b4f-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="39b4f-124">Anwendungen, die die Nachrichten Warteschlange anschließen, sehen weiterhin das alte Dialogfeld Layout.</span><span class="sxs-lookup"><span data-stu-id="39b4f-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="39b4f-125">Anwendungen, die ihre eigenen Vorlagen bereitstellen, werden Sie weiterhin verwenden können.</span><span class="sxs-lookup"><span data-stu-id="39b4f-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="39b4f-126">Anwendungen, die die neuen Vorlagen nicht erhalten, sehen keine Dialog layoutlayoutänderungen von Vista.</span><span class="sxs-lookup"><span data-stu-id="39b4f-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="39b4f-127">Sie sollten jedoch immer noch die neue WYSIWYG-Schriftart Vorschau erhalten.</span><span class="sxs-lookup"><span data-stu-id="39b4f-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="39b4f-128">**Schriftarten anzeigen/ausblenden**</span><span class="sxs-lookup"><span data-stu-id="39b4f-128">**Show/hide fonts**</span></span>

<span data-ttu-id="39b4f-129">Für alle Versionen von Choice Font werden im Dialogfeld die Schriftart Einstellungen für das Anzeigen/Ausblenden des aktuellen Benutzers verwendet, um die anzuzeigende Schriftart Liste zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="39b4f-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="39b4f-130">Dies führt dazu, dass in den meisten Fällen weniger Schriftart Listen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39b4f-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="39b4f-131">Entschärfung durch Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="39b4f-131">End-user Mitigation</span></span>

<span data-ttu-id="39b4f-132">**Schriftarten anzeigen/ausblenden:** Um das Ausblenden der Schriftart zu deaktivieren, sollten Benutzer in der Schriftarten-cpl zur Seite Schriftart Einstellungen wechseln und die Option "</span><span class="sxs-lookup"><span data-stu-id="39b4f-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="39b4f-133">Kontrollkästchen "Schriftarten basierend auf Spracheinstellungen ausblenden"</span><span class="sxs-lookup"><span data-stu-id="39b4f-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="39b4f-134">Entwickler Entschärfung</span><span class="sxs-lookup"><span data-stu-id="39b4f-134">Developer Mitigation</span></span>

-   <span data-ttu-id="39b4f-135">**Visuelle Aktualisierung:** Anwendungsentwickler, die eigene Vorlagen bereitstellen, können diese aktualisieren, damit Sie mit der entsprechenden neuen Vorlage für Windows 7 übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="39b4f-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="39b4f-136">Die neuen Vorlagen sind in der Vorlagen Datei Font. DLG verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39b4f-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="39b4f-137">**Hinweis:** Die neue veröffentlichte Vorlage enthält ein zusätzliches Syslink-Steuerelement, das eine Verknüpfung bereitstellt, mit der Benutzer die Schriftarten-cpl starten können, um weitere Schriftarten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39b4f-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="39b4f-138">Das Link Steuerelement erfordert Version 6 der allgemeinen Windows-Steuerelement Bibliothek (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="39b4f-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="39b4f-139">Entwickler sollten ein Manifest oder eine Direktive bereitstellen, das die Verwendung von Version 6 der DLL angibt, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39b4f-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="39b4f-140">Verwenden Sie stattdessen den Steuer Objekttyp "PUSHBUTTON", wenn eine Anwendung eine frühere Version der allgemeinen Steuerelement Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="39b4f-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="39b4f-141">**Schriftarten anzeigen/ausblenden:** Entwickler können diese Funktion deaktivieren, indem Sie ein zusätzliches Flag (CF \_ inactivefonts) im Flags-Member der choosefont-Struktur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="39b4f-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="39b4f-142">Das Festlegen dieses Flags bewirkt, dass alle installierten Schriftarten in der Schriftart Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39b4f-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="39b4f-143">**Schriftarten anzeigen/ausblenden:** Anwendungen, die Hilfe Inhalte zur Auswahl von Informationen bereitstellen, möchten möglicherweise Inhalt hinzufügen, um zu erklären, warum die Schriftart Liste reduziert ist, und die Benutzer an die Schriftarten-cpl weiterleiten, um deren Schriftart</span><span class="sxs-lookup"><span data-stu-id="39b4f-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="39b4f-144">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="39b4f-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="39b4f-145">Entwickler, deren Anwendungen die ausgewählte Meldungs Warteschlange zum Anpassen des Dialog Felds anschließen, sollten überprüfen, ob Ihre Anwendungen alle vorhandenen Funktionen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="39b4f-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="39b4f-146">Anwendungen, die die Schriftart Liste stark mithilfe von Flags kürzen, sollten sicherstellen, dass die Liste der dargestellten Schriftart weiterhin akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="39b4f-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



