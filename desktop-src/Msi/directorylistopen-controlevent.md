---
description: Mit diesem Ereignis wird ein Verzeichnis im directerylist-Steuerelement ausgewählt und hervorgehoben, das vom Benutzer geöffnet werden soll. Weitere Informationen finden Sie unter Dialog Feld "Durchsuchen".
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: Director-listopen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218850"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="728e8-104">Director-listopen ControlEvent</span><span class="sxs-lookup"><span data-stu-id="728e8-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="728e8-105">Mit diesem Ereignis wird ein Verzeichnis im [directerylist-Steuer](directorylist-control.md) Element ausgewählt und hervorgehoben, das vom Benutzer geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="728e8-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="728e8-106">Weitere Informationen finden Sie unter [Dialog Feld "Durchsuchen](browse-dialog.md)".</span><span class="sxs-lookup"><span data-stu-id="728e8-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="728e8-107">Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert.</span><span class="sxs-lookup"><span data-stu-id="728e8-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="728e8-108">Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="728e8-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="728e8-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="728e8-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="728e8-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="728e8-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="728e8-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="728e8-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="728e8-112">Wenn kein Verzeichnis im [Director List-Steuer](directorylist-control.md)Element ausgewählt wurde, deaktiviert ein Ereignis vom Datentyp directoriylistopen alle anderen Steuerelemente, die ein directoriylistopen-Ereignis veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="728e8-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="728e8-113">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="728e8-113">Published By</span></span>

[<span data-ttu-id="728e8-114">Directoren auflisten</span><span class="sxs-lookup"><span data-stu-id="728e8-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="728e8-115">Argument</span><span class="sxs-lookup"><span data-stu-id="728e8-115">Argument</span></span>

<span data-ttu-id="728e8-116">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="728e8-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="728e8-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="728e8-117">Action on Subscribers</span></span>

<span data-ttu-id="728e8-118">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="728e8-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="728e8-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="728e8-119">Typical Use</span></span>

<span data-ttu-id="728e8-120">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie Director List wird verwendet, um die Schritt Ausführung im Pfad zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="728e8-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



