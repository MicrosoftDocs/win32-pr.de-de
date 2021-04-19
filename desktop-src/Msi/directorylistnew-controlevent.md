---
description: Dieses Ereignis benachrichtigt das directorylist-Steuerelement, dass ein neuer Ordner erstellt werden muss. Er erstellt den neuen Ordner und wählt das Namensfeld des Ordners für die Bearbeitung aus.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: Director-listnew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366338"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="c5ede-103">Director-listnew ControlEvent</span><span class="sxs-lookup"><span data-stu-id="c5ede-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="c5ede-104">Dieses Ereignis benachrichtigt das [directorylist-Steuer](directorylist-control.md) Element, dass ein neuer Ordner erstellt werden muss. Er erstellt den neuen Ordner und wählt das Namensfeld des Ordners für die Bearbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="c5ede-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="c5ede-105">Der Standardname des neuen Ordners kann in der [UIText-Tabelle](uitext-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5ede-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="c5ede-106">Geben Sie "NewFolder" in die Schlüssel Spalte ein.</span><span class="sxs-lookup"><span data-stu-id="c5ede-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="c5ede-107">Geben Sie den Wert für den Standardnamen des neuen Ordners in die Text Spalte ein.</span><span class="sxs-lookup"><span data-stu-id="c5ede-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="c5ede-108">Dieser Wert muss in Form eines Datentyps der [Dateiname](filename.md) -Spalte vorliegen und die SFN- \| LFN-Syntax verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5ede-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="c5ede-109">Wenn dieser Wert in der UIText-Tabelle nicht vorhanden ist oder ein ungültiger Wert ist, verwendet das Installationsprogramm den Standardwert "fldr \| New Folder".</span><span class="sxs-lookup"><span data-stu-id="c5ede-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="c5ede-110">Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".</span><span class="sxs-lookup"><span data-stu-id="c5ede-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="c5ede-111">Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert.</span><span class="sxs-lookup"><span data-stu-id="c5ede-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="c5ede-112">Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5ede-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="c5ede-113">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5ede-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c5ede-114">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c5ede-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c5ede-115">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c5ede-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="c5ede-116">Beachten Sie Folgendes: Wenn dieses ControlEvent erneut aufgerufen wird, wenn ein neuer Ordner bereits vorhanden ist, wird kein zweiter neuer Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="c5ede-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="c5ede-117">In diesem Fall wählt der Aufruf von directorylistnew den Namen des vorhandenen neuen Ordners für die Bearbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="c5ede-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="c5ede-118">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="c5ede-118">Published By</span></span>

[<span data-ttu-id="c5ede-119">Directoren auflisten</span><span class="sxs-lookup"><span data-stu-id="c5ede-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="c5ede-120">Argument</span><span class="sxs-lookup"><span data-stu-id="c5ede-120">Argument</span></span>

<span data-ttu-id="c5ede-121">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="c5ede-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c5ede-122">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="c5ede-122">Action on Subscribers</span></span>

<span data-ttu-id="c5ede-123">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="c5ede-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c5ede-124">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="c5ede-124">Typical Use</span></span>

<span data-ttu-id="c5ede-125">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie das directorylist-Objekt wird verwendet, um die Erstellung eines neuen Ordners zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c5ede-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



