---
description: Einige Typen, die von TSPI definiert werden, sind nicht transparente Handles.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Nicht transparente Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527098"
---
# <a name="opaque-handles"></a><span data-ttu-id="bc761-103">Nicht transparente Handles</span><span class="sxs-lookup"><span data-stu-id="bc761-103">Opaque Handles</span></span>

<span data-ttu-id="bc761-104">Einige Typen, die von TSPI definiert werden, sind nicht transparente Handles.</span><span class="sxs-lookup"><span data-stu-id="bc761-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="bc761-105">Diese werden in TSPI als öffentliche Verweise auf private Datenstrukturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc761-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="bc761-106">Dies ermöglicht die Typüberprüfung von Parametern, die für die Schnittstellen Prozeduren bereitgestellt werden, während trotzdem ein Measure vom Typ "Protection"</span><span class="sxs-lookup"><span data-stu-id="bc761-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="bc761-107">Nur der Besitzer der privaten Datenstruktur weiß, wie der nicht transparente Typ als Verweis auf seine Datenstruktur Darstellung interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc761-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="bc761-108">Als Beispiel für die Verwendung von nicht transparenten Handles sollten Sie ein Telefongerät in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="bc761-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="bc761-109">TAPI und der Dienstanbieter verwalten in der Regel Datenstrukturen, die die jeweiligen Ansichten des Geräts darstellen.</span><span class="sxs-lookup"><span data-stu-id="bc761-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="bc761-110">In typischen Telefondaten Strukturen, die von TAPI und einem Dienstanbieter verwaltet werden, enthält jedes ein undurchsichtiges Handle für die andere Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="bc761-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="bc761-111">Diese wurden in einem frühen Initialisierungs Schritt ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="bc761-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="bc761-112">Wenn TAPI eine TSPI-Funktion aufruft, übergibt er das nicht transparente handle, um auf das Gerät zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="bc761-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="bc761-113">Der Dienstanbieter weiß, wie dieser als Verweis (Pfeil) zur Datenstruktur aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc761-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="bc761-114">Ein ähnlicher Prozess tritt auf, wenn der Dienstanbieter eine Rückruffunktion in TAPI aufruft.</span><span class="sxs-lookup"><span data-stu-id="bc761-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



