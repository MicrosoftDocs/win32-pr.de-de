---
title: Optionen für das UI-Plug-in
description: Optionen für das UI-Plug-in
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Windows Media Player-Plug-ins, Optionen
- Plug-ins, Optionen
- Plug-Ins für Benutzeroberflächen, Optionen
- UI-Plug-ins, Optionen
- Einstellungs Bereichs-Plug-ins
- Background-Plug-ins
- separate Fenster-Plug-ins
- Metadatenbereich-Plug-ins
- Anzeige Bereichs-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342039"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="5eded-112">Optionen für das UI-Plug-in</span><span class="sxs-lookup"><span data-stu-id="5eded-112">UI Plug-in Options</span></span>

<span data-ttu-id="5eded-113">Alle fünf Benutzeroberflächen-Plug-in-Typen können über eine Eigenschaften Seite verfügen, auf der der Benutzer die Plug-in-Einstellungen ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5eded-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="5eded-114">Diese Eigenschaften Seite kann so festgelegt werden, dass Sie automatisch angezeigt wird, wenn ein Plug-in zum ersten Mal geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5eded-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="5eded-115">Sie können auch über die Registerkarte Plug-ins im Dialogfeld Optionen auf Sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5eded-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="5eded-116">Ein UI-Plug-in kann so festgelegt werden, dass es nach der Installation automatisch geladen wird, wenn Windows Media Player gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5eded-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="5eded-117">Wenn Sie nicht automatisch gestartet wird, kann der Benutzer Sie laden, indem er Sie aus der Liste der **Plug-ins** **im Menü Extras** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5eded-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="5eded-118">Ein Anzeige Bereichs-Plug-in kann über mehrere Voreinstellungen verfügen, bei denen es sich um unterschiedliche Ansichten handelt, die das Plug-in für den Benutzer verfügbar machen kann.</span><span class="sxs-lookup"><span data-stu-id="5eded-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="5eded-119">Der Benutzer kann die Voreinstellung ändern, indem er im Menü **Ansicht** einen anderen Eintrag aus der Liste **Visualisierungen und Sichten** oder mithilfe der Pfeil Schaltflächen am unteren Rand des Fensters jetzt wieder **Gabe** direkt oberhalb der Statusmeldungs-und Transport Steuerelemente auswählt.</span><span class="sxs-lookup"><span data-stu-id="5eded-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="5eded-120">Benutzeroberflächen-Plug-ins im Hintergrund und in separaten Fenstern können so programmiert werden, dass Sie ein Medien Element oder eine Wiedergabeliste akzeptieren, die der Benutzer an Sie sendet</span><span class="sxs-lookup"><span data-stu-id="5eded-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="5eded-121">Wenn diese Funktion von einem Plug-in unterstützt wird, wird der Name in der Liste **Senden an** angezeigt, die im Kontextmenü des Wiedergabelisten-Steuer Elements oder der Bibliothek verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5eded-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="5eded-122">Ein UI-Plug-in kann so programmiert werden, dass Tastenkombinationen abgefangen werden, wenn es den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="5eded-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="5eded-123">Der Tastaturfokus ist erforderlich, um Konflikte zu verhindern, wenn mehrere UI-Plug-Ins geladen werden, die dieselbe Tastenkombination abfangen.</span><span class="sxs-lookup"><span data-stu-id="5eded-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="5eded-124">Obwohl dies Konflikte verhindert, kann dies auch Verwirrung für Endbenutzer verursachen.</span><span class="sxs-lookup"><span data-stu-id="5eded-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="5eded-125">Aus diesem Grund wird die Verwendung von Tastenkombinationen mit UI-Plug-ins nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5eded-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="5eded-126">Wenn Sie verwendet werden, sollten Sie jedoch keine Tastenkombinationen abfangen, die von Windows Media Player verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eded-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="5eded-127">Eine umfassende Liste der Tastenkombinationen, die vom Player verwendet werden, finden Sie in der Hilfe zu Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5eded-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eded-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5eded-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eded-129">**Übersicht über das UI-Plug-in**</span><span class="sxs-lookup"><span data-stu-id="5eded-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




