---
description: Dieses Ereignis benachrichtigt das Installationsprogramm, während das vorhandene Dialogfeld weiterhin ausgeführt wird, dass eine Funktion oder alle Funktionen von der Quelle ausgeführt werden sollen.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: Addsource-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360488"
---
# <a name="addsource-controlevent"></a><span data-ttu-id="2ff72-103">Addsource-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2ff72-103">AddSource ControlEvent</span></span>

<span data-ttu-id="2ff72-104">Dieses Ereignis benachrichtigt das Installationsprogramm, während das vorhandene Dialogfeld weiterhin ausgeführt wird, dass eine Funktion oder alle Funktionen von der Quelle ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ff72-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run from source.</span></span> <span data-ttu-id="2ff72-105">Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="2ff72-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="2ff72-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ff72-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2ff72-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ff72-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2ff72-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2ff72-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2ff72-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2ff72-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2ff72-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="2ff72-110">Published By</span></span>

<span data-ttu-id="2ff72-111">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2ff72-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="2ff72-112">Argument</span><span class="sxs-lookup"><span data-stu-id="2ff72-112">Argument</span></span>

<span data-ttu-id="2ff72-113">Eine Zeichenfolge, entweder der Name der Funktion oder "All".</span><span class="sxs-lookup"><span data-stu-id="2ff72-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2ff72-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="2ff72-114">Action on Subscribers</span></span>

<span data-ttu-id="2ff72-115">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="2ff72-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2ff72-116">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="2ff72-116">Typical Use</span></span>

<span data-ttu-id="2ff72-117">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um das Installationsprogramm zu benachrichtigen, ohne das Dialogfeld zu beenden.</span><span class="sxs-lookup"><span data-stu-id="2ff72-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



