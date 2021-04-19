---
description: Dieses modale Dialogfeld ermöglicht es Benutzern, bestimmte Elemente auszuwählen.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Auswahl Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349715"
---
# <a name="selection-dialog"></a><span data-ttu-id="3b62e-103">Auswahl Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="3b62e-103">Selection Dialog</span></span>

<span data-ttu-id="3b62e-104">Dieses modale Dialogfeld ermöglicht es Benutzern, bestimmte Elemente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3b62e-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="3b62e-105">Ein Auswahl Dialogfeld enthält ein [SelectionTree-Steuer](selectiontree-control.md) Element, mit dem mehrere ControlEvents veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="3b62e-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="3b62e-106">Häufig werden diese ControlEvents von [Text](text-control.md)-, [Symbol](icon-control.md)-oder [Bitmap](bitmap-control.md) -Steuerelementen abonniert, die eine Beschreibung, die Größe, den Pfad und das Symbol des hervorgehobenen Elements anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3b62e-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="3b62e-107">Das Dialogfeld enthält ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element, das den [selectionbrowse-ControlEvent](selectionbrowse-controlevent.md) veröffentlicht und ein [Dialogfeld zum Durchsuchen](browse-dialog.md)erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3b62e-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="3b62e-108">Das Browse-Steuerelement ermöglicht es dem Benutzer, ein Verzeichnis auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3b62e-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="3b62e-109">Die Auswahl Struktur wird erst aufgefüllt, nachdem die Aktion " [costinitialize](costinitialize-action.md) " und die [Aktion "costfinalize](costfinalize-action.md) " aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3b62e-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="3b62e-110">Ein Auswahl Dialogfeld wird häufig verwendet, um Features auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3b62e-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="3b62e-111">Die Funktionen werden in einem SelectionTree-Steuerelement als Elemente aufgeführt und mit der kurzen Text Zeichenfolge gekennzeichnet, die in der Spalte Titel der [Featuretabelle](feature-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b62e-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="3b62e-112">Die Text Zeichenfolge in der Spalte Beschreibung der Funktions Tabelle wird als [selectiondescription ControlEvent](selectiondescription-controlevent.md) veröffentlicht und durch ein [Text-Steuer](text-control.md) Element im Auswahl Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b62e-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="3b62e-113">Das Auswahl Struktur-Steuerelement veröffentlicht auch das Handle für das Symbol des hervorgehobenen Elements.</span><span class="sxs-lookup"><span data-stu-id="3b62e-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



