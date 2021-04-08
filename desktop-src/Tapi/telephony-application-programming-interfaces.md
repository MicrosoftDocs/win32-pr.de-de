---
description: Die Microsoft Telefonie-Anwendungs Programmierschnittstellen unterstützen die Entwicklung von Kommunikationsanwendungen für Microsoft Windows. Die Telefonieschnittstellen sind in der folgenden Tabelle aufgeführt.
ms.assetid: e7348296-ee2d-4e0a-b274-3563dccea841
title: Telefonie-Anwendungs Programmierschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19fd6a520c8a53440967eeef753b7ed8c90ba5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868147"
---
# <a name="telephony-application-programming-interfaces"></a><span data-ttu-id="6dd12-104">Telefonie-Anwendungs Programmierschnittstellen</span><span class="sxs-lookup"><span data-stu-id="6dd12-104">Telephony Application Programming Interfaces</span></span>

<span data-ttu-id="6dd12-105">Die Microsoft Telefonie-Anwendungs Programmierschnittstellen unterstützen die Entwicklung von Kommunikationsanwendungen für Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6dd12-105">The Microsoft telephony application programming interfaces support the development of communications applications for Microsoft Windows.</span></span> <span data-ttu-id="6dd12-106">Die Telefonieschnittstellen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dd12-106">The telephony interfaces are listed in the following table.</span></span>



| <span data-ttu-id="6dd12-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6dd12-107">Interface</span></span>                                                  | <span data-ttu-id="6dd12-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dd12-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dd12-109">TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="6dd12-109">TAPI 2.x</span></span>](./tapi-2-2-start-page.md)               | <span data-ttu-id="6dd12-110">Eine auf C-Programmiersprachen basierende API, mit der Sie Kommunikationsanwendungen implementieren können, die von einem einfachen Modem Steuerelement bis hin zu Callcenter mit mehreren Agents und Switches reichen.</span><span class="sxs-lookup"><span data-stu-id="6dd12-110">A C-programming language based API that enables you to implement communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="6dd12-111">TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="6dd12-111">TAPI 3.x</span></span>](tapi-3-1-start-page.md)                        | <span data-ttu-id="6dd12-112">Eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="6dd12-112">A COM-based API that merges classic and IP telephony.</span></span>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6dd12-113">TSPI</span><span class="sxs-lookup"><span data-stu-id="6dd12-113">TSPI</span></span>](./telephony-service-providers-start-page.md) | <span data-ttu-id="6dd12-114">Bei einem Telefoniedienstanbieter (TSP) handelt es sich um eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6dd12-114">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="6dd12-115">Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt Informationen an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6dd12-115">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span> |
| [<span data-ttu-id="6dd12-116">MSPi</span><span class="sxs-lookup"><span data-stu-id="6dd12-116">MSPI</span></span>](media-service-providers-start-page.md)             | <span data-ttu-id="6dd12-117">Ein Medien Dienstanbieter (MSP) ermöglicht einer Anwendung eine beträchtliche Kontrolle über die Medien für einen bestimmten Transportmechanismus.</span><span class="sxs-lookup"><span data-stu-id="6dd12-117">A media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="6dd12-118">Ein MSP wird immer einem Telefoniedienstanbieter (TSP) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6dd12-118">An MSP is always paired with a telephony service provider (TSP).</span></span>                                                                                                                                                         |



 

 

 
