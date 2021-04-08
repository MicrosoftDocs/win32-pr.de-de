---
title: Windows (Entwurfs Grundlagen)
description: Windows sind die wichtigsten \ 0034; kanvasen \ 0034; oder Benutzeroberflächen Oberflächen ihrer Desktop-App, einschließlich der Hauptfenster selbst und Popups, Dialogfelder und Assistenten. Beachten Sie diese Richtlinien, wenn Sie entscheiden, welche Oberfläche verwendet werden soll und wie Sie Sie am besten verwenden
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961075"
---
# <a name="windows-design-basics"></a><span data-ttu-id="cdb75-104">Windows (Entwurfs Grundlagen)</span><span class="sxs-lookup"><span data-stu-id="cdb75-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="cdb75-105">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cdb75-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="cdb75-106">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="cdb75-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="cdb75-107">Bei Windows handelt es sich um die Hauptfenster der Benutzeroberfläche Ihrer Desktop-App, einschließlich der Hauptfenster selbst und Popups, Dialogfelder und Assistenten.</span><span class="sxs-lookup"><span data-stu-id="cdb75-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="cdb75-108">Beachten Sie diese Richtlinien, wenn Sie entscheiden, welche Oberfläche verwendet werden soll und wie Sie Sie am besten verwenden</span><span class="sxs-lookup"><span data-stu-id="cdb75-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cdb75-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cdb75-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdb75-110">Thema</span><span class="sxs-lookup"><span data-stu-id="cdb75-110">Topic</span></span></th>
<th><span data-ttu-id="cdb75-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdb75-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cdb75-112"><a href="win-window-mgt.md">Fensterverwaltung</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-113">Dieser Artikel befasst sich mit der Standard Platzierung von Windows, wenn Sie anfänglich auf dem Bildschirm angezeigt wird, der Stapelreihenfolge relativ zu anderen Fenstern (<a href="glossary.md">Z-Reihenfolge</a>), der Anfangs Größe und der Auswirkung der Anzeige auf den Eingabefokus</span><span class="sxs-lookup"><span data-stu-id="cdb75-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdb75-114"><a href="win-window-frames.md">Fensterrahmen</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-115">Die meisten Programme sollten Standardfenster Rahmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdb75-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="cdb75-116">Immersive Anwendungen können über einen Vollbildmodus verfügen, der den Fensterrahmen verbirgt.</span><span class="sxs-lookup"><span data-stu-id="cdb75-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="cdb75-117">Sie sollten Glas strategisch für ein einfacheres, helleres aussehen in Erwägung gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="cdb75-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdb75-118"><a href="win-dialog-box.md">Dialog Felder</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-119">Ein Dialogfeld ist ein sekundäres Fenster, das es Benutzern ermöglicht, einen Befehl auszuführen, Benutzer zu einer Frage zu bitten oder Benutzern Informationen oder ein Fortschritts Feedback bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cdb75-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdb75-120"><a href="win-common-dlg.md">Allgemeine Dialogfelder</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-121">Die allgemeinen Microsoft Windows-Dialoge bestehen aus den Dialogfeldern Datei öffnen, Datei speichern, Ordner öffnen, suchen und ersetzen, drucken, Seite einrichten, Schriftart und Farbe.</span><span class="sxs-lookup"><span data-stu-id="cdb75-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdb75-122"><a href="win-wizards.md">Assistenten</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-123">Trotz dieses wunderbaren namens sind die Assistenten nicht wirklich eine besondere Form der Benutzeroberfläche, und Sie verfügen nur über einen bestimmten Bereich von Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="cdb75-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdb75-124"><a href="win-property-win.md">Eigenschaften Fenster</a></span><span class="sxs-lookup"><span data-stu-id="cdb75-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="cdb75-125">Das Eigenschaften Fenster ist der Sammelname für die folgenden Typen von Benutzeroberflächen (User Interfaces, UIs):</span><span class="sxs-lookup"><span data-stu-id="cdb75-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="cdb75-126">Eigenschaften Blatt: wird zum <strong>anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Sammlung von Objekten in einem Dialogfeld</strong>verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb75-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="cdb75-127">Eigenschaften Inspektor: wird zum <strong>anzeigen und Ändern von Eigenschaften für ein Objekt oder eine Sammlung von Objekten in einem</strong>Bereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdb75-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="cdb75-128">Optionen (Dialogfeld): dient zum <strong>anzeigen und Ändern von Optionen für eine Anwendung</strong>.</span><span class="sxs-lookup"><span data-stu-id="cdb75-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

