---
title: Joystick Funktionen
description: Joystick Funktionen
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- Multimedia-Eingabe, Joysticks
- Joysticks, zwei Achsenbewegung
- Joysticks, drei Achsenbewegung
- Joysticks, Schaltflächen
- Joysticks, bewegungsbereiche
- Joysticks, Abruf Häufigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726720"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="6c1a4-109">Joystick Funktionen</span><span class="sxs-lookup"><span data-stu-id="6c1a4-109">Joystick Capabilities</span></span>

<span data-ttu-id="6c1a4-110">Joysticks können eine Bewegung mit zwei oder drei Achsen und bis zu vier Schaltflächen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="6c1a4-111">Außerdem unterstützen Joysticks verschiedene *Bereiche von Bewegungs* -und Abruf *Frequenzen*.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="6c1a4-112">Der Bewegungsbereich ist die Distanz, die ein Joystick Handle von seiner Ruheposition an die Position von der Ruheposition aus verschieben kann.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="6c1a4-113">Die Abruf Häufigkeit ist das Zeitintervall zwischen den Joystick Abfragen.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="6c1a4-114">Joystick Treiber können entweder einen oder zwei Joysticks unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="6c1a4-115">Sie können die Anzahl von Joystick ermitteln, die von einem Joystick Treiber unterstützt werden, indem Sie die Funktion " [**joygetnumdebug**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="6c1a4-116">Diese Funktion gibt eine ganze Zahl ohne Vorzeichen zurück, die die Anzahl unterstützter Joystick enthält, oder 0 (null), wenn keine Joystick Unterstützung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="6c1a4-117">Der Rückgabewert gibt nicht die Anzahl von Joystick an, die an das System angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="6c1a4-118">Mithilfe der [**joygetpos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) -Funktion können Sie feststellen, ob ein Joystick mit dem System verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="6c1a4-119">Diese Funktion gibt "joyerr noError" zurück, \_ Wenn das angegebene Gerät angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="6c1a4-120">Andernfalls wird das joyerr-paar nicht getrennt zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="6c1a4-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="6c1a4-121">Jeder Joystick verfügt über mehrere Funktionen, die für Ihre Anwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="6c1a4-122">Sie können die Funktionen eines Joystick mithilfe der [**joygetdevcaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="6c1a4-123">Diese Funktion füllt eine [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) -Struktur mit Joystick Funktionen aus, z. b. die minimalen und maximalen Werte für das Koordinatensystem, die Anzahl der Schaltflächen auf dem Joystick und die minimalen und maximalen Abruf Frequenzen.</span><span class="sxs-lookup"><span data-stu-id="6c1a4-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 