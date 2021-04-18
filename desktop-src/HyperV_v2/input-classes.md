---
description: Die Benutzereingabe Geräte werden durch diese Klassen dargestellt. Ein virtueller Computer verfügt immer über eine Instanz jeder zugeordneten Klasse.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Eingabe Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345229"
---
# <a name="input-classes"></a><span data-ttu-id="b5340-104">Eingabe Klassen</span><span class="sxs-lookup"><span data-stu-id="b5340-104">Input classes</span></span>

<span data-ttu-id="b5340-105">Die Benutzereingabe Geräte werden durch diese Klassen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b5340-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="b5340-106">Ein virtueller Computer verfügt immer über eine Instanz jeder zugeordneten Klasse.</span><span class="sxs-lookup"><span data-stu-id="b5340-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="b5340-107">Diese Geräte können nicht zum virtuellen Computer hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b5340-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="b5340-108">Daher sind keine Ressourcenpool Instanzen für Tastatur-oder Maus Geräte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b5340-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="b5340-109">Tastatur-und Maus Geräte sind über die [**MSVM- \_ systemgerätezuordnung**](msvm-systemdevice.md) mit dem virtuellen Computer verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b5340-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="b5340-110">Ein virtueller Computer enthält sowohl einen PS2 als auch ein synthetisches Mausgerät.</span><span class="sxs-lookup"><span data-stu-id="b5340-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="b5340-111">Es ist jeweils nur ein Zeigegerät aktiv.</span><span class="sxs-lookup"><span data-stu-id="b5340-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="b5340-112">Im folgenden finden Sie WMI-Klassen für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="b5340-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b5340-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b5340-113">In this section</span></span>



| <span data-ttu-id="b5340-114">Thema</span><span class="sxs-lookup"><span data-stu-id="b5340-114">Topic</span></span>                                                          | <span data-ttu-id="b5340-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5340-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="b5340-116">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="b5340-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="b5340-117">Stellt ein Tastatur Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="b5340-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="b5340-118">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="b5340-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="b5340-119">Stellt ein PS2-Mausgerät dar.</span><span class="sxs-lookup"><span data-stu-id="b5340-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="b5340-120">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="b5340-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="b5340-121">Stellt ein synthetisches Mausgerät dar.</span><span class="sxs-lookup"><span data-stu-id="b5340-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




