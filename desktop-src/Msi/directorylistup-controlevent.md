---
description: Dieses Ereignis benachrichtigt das Director List-Steuerelement, dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte. Weitere Informationen finden Sie unter Dialog Feld "Durchsuchen".
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: Director-listup-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961005"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="e27df-104">Director-listup-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="e27df-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="e27df-105">Dieses Ereignis benachrichtigt das [Director List-Steuer](directorylist-control.md) Element, dass der Benutzer das übergeordnete Element des aktuellen Verzeichnisses auswählen möchte.</span><span class="sxs-lookup"><span data-stu-id="e27df-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="e27df-106">Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".</span><span class="sxs-lookup"><span data-stu-id="e27df-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="e27df-107">Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert.</span><span class="sxs-lookup"><span data-stu-id="e27df-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="e27df-108">Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e27df-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e27df-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e27df-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e27df-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e27df-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e27df-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e27df-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e27df-112">Handelt es sich bei dem aktuellen Verzeichnis um das Stammverzeichnis des Laufwerks, werden alle anderen Steuerelemente, die ein Director-listup-Ereignis veröffentlichen, von einem directoriylistup-Ereignis deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e27df-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="e27df-113">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="e27df-113">Published By</span></span>

[<span data-ttu-id="e27df-114">Directoren auflisten</span><span class="sxs-lookup"><span data-stu-id="e27df-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="e27df-115">Argument</span><span class="sxs-lookup"><span data-stu-id="e27df-115">Argument</span></span>

<span data-ttu-id="e27df-116">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="e27df-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e27df-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e27df-117">Action on Subscribers</span></span>

<span data-ttu-id="e27df-118">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="e27df-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e27df-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="e27df-119">Typical Use</span></span>

<span data-ttu-id="e27df-120">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie Director List wird verwendet, um eine Schritt-für-Schritt-Ausführung des Pfads zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e27df-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



