---
description: Andere TAPI-Telefonfunktionen verwenden ein Handle für ein geöffnetes Telefongerät, um das geöffnete Telefongerät zu identifizieren.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: Geräte-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348404"
---
# <a name="device-ids"></a><span data-ttu-id="e2b8a-103">Geräte-IDs</span><span class="sxs-lookup"><span data-stu-id="e2b8a-103">Device IDs</span></span>

<span data-ttu-id="e2b8a-104">Andere TAPI-Telefonfunktionen verwenden ein Handle für ein geöffnetes Telefongerät, um das geöffnete Telefongerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="e2b8a-105">Die einzigen Funktionen für Telefongeräte, die einen Parameter für einen Telefongeräte Bezeichner verwenden (im Gegensatz zu einem Telefon handle), sind die [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) -und [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="e2b8a-106">Eine Anwendung kann den Geräte Bezeichner des Telefons abrufen, indem er die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion mit dem Telefon Handle als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="e2b8a-107">Eine Anwendung kann auch Geräte Bezeichner für verschiedene Geräteklassen abrufen, die einem geöffneten Telefon zugeordnet sind, indem [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="e2b8a-108">Weitere Informationen finden Sie unter [TAPI-Geräteklassen](tapi-device-classes.md) für Geräteklassen Namen.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="e2b8a-109">Diese Funktion nimmt einen Telefon Handle und eine Beschreibung der Geräteklasse an.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="e2b8a-110">Er gibt den Geräte Bezeichner für das Gerät der angegebenen Geräteklasse zurück, die dem geöffneten Telefongerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="e2b8a-111">Wenn die Geräteklasse "TAPI/Phone" ist, wird der Geräte Bezeichner des Telefon Geräts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="e2b8a-112">Im Gegensatz zu Linien Geräten, für die die grundlegenden Zeilen Dienste die Entsprechung von Töpfen bereitstellen, wird für Telefongeräte kein minimal garantierter Satz von Funktionen definiert.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="e2b8a-113">Obwohl jedes Telefongerät mindestens die in diesem Abschnitt beschriebenen Funktionen und Nachrichten bereitstellt, bieten Sie keine tatsächlichen Vorgänge auf dem physischen Telefongerät an.</span><span class="sxs-lookup"><span data-stu-id="e2b8a-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



