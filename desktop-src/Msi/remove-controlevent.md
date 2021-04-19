---
description: Das Installationsprogramm wird durch dieses Ereignis benachrichtigt, wenn ein Feature oder alle Funktionen zum Entfernen ausgewählt werden, während das vorhandene Dialogfeld weiterhin ausgeführt wird.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: ControlEvent entfernen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373047"
---
# <a name="remove-controlevent"></a><span data-ttu-id="61841-103">ControlEvent entfernen</span><span class="sxs-lookup"><span data-stu-id="61841-103">Remove ControlEvent</span></span>

<span data-ttu-id="61841-104">Das Installationsprogramm wird durch dieses Ereignis benachrichtigt, wenn ein Feature oder alle Funktionen zum Entfernen ausgewählt werden, während das vorhandene Dialogfeld weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61841-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="61841-105">Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="61841-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="61841-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="61841-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="61841-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61841-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="61841-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61841-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="61841-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="61841-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="61841-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="61841-110">Published By</span></span>

<span data-ttu-id="61841-111">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="61841-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="61841-112">Argument</span><span class="sxs-lookup"><span data-stu-id="61841-112">Argument</span></span>

<span data-ttu-id="61841-113">Eine Zeichenfolge, die entweder der Name der Funktion oder "All" ist.</span><span class="sxs-lookup"><span data-stu-id="61841-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="61841-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="61841-114">Action on Subscribers</span></span>

<span data-ttu-id="61841-115">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="61841-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="61841-116">Aktion nach Verleger beim Aktivieren des Abonnenten</span><span class="sxs-lookup"><span data-stu-id="61841-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="61841-117">Das Installationsprogramm speichert das vorhandene Dialogfeld und benachrichtigt das Installationsprogramm.</span><span class="sxs-lookup"><span data-stu-id="61841-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="61841-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="61841-118">Typical Use</span></span>

<span data-ttu-id="61841-119">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld, das an dieses Ereignis gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="61841-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



