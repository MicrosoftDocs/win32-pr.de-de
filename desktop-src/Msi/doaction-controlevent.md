---
description: Das doaction ControlEvent benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen. Dieses Ereignis kann durch ein PUSHBUTTON-Steuerelement, ein CheckBox-Steuerelement oder ein SelectionTree-Steuerelement veröffentlicht werden. Dieses Ereignis sollte in der Tabelle ControlEvent erstellt werden.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Doaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128388"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="59aa2-105">Doaction ControlEvent</span><span class="sxs-lookup"><span data-stu-id="59aa2-105">DoAction ControlEvent</span></span>

<span data-ttu-id="59aa2-106">Das doaction ControlEvent benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="59aa2-107">Dieses Ereignis kann durch ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement, ein [CheckBox](checkbox-control.md) -Steuerelement oder ein [SelectionTree](selectiontree-control.md) -Steuerelement veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="59aa2-108">Dieses Ereignis sollte in der Tabelle [ControlEvent](controlevent-table.md) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="59aa2-109">Beachten Sie, dass benutzerdefinierte Aktionen, die von einem doaction ControlEvent gestartet werden, eine Nachricht mit der [**Message-Methode**](session-message.md)senden können, aber keine Nachricht mit [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)senden können.</span><span class="sxs-lookup"><span data-stu-id="59aa2-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="59aa2-110">Auf Systemen vor Windows Server 2003 können benutzerdefinierte Aktionen, die von einem doaction ControlEvent gestartet werden, keine Nachrichten mit der **msiprocessmessage** oder der **Message-Methode** senden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="59aa2-111">Weitere Informationen finden Sie unter [Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md)".</span><span class="sxs-lookup"><span data-stu-id="59aa2-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="59aa2-112">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59aa2-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="59aa2-113">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="59aa2-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="59aa2-114">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="59aa2-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="59aa2-115">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="59aa2-115">Published By</span></span>

<span data-ttu-id="59aa2-116">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="59aa2-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="59aa2-117">Argument</span><span class="sxs-lookup"><span data-stu-id="59aa2-117">Argument</span></span>

<span data-ttu-id="59aa2-118">Eine Zeichenfolge, der Name der benutzerdefinierten Aktion, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59aa2-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="59aa2-119">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="59aa2-119">Action on Subscribers</span></span>

<span data-ttu-id="59aa2-120">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="59aa2-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="59aa2-121">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="59aa2-121">Typical Use</span></span>

<span data-ttu-id="59aa2-122">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um eine benutzerdefinierte Aktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



