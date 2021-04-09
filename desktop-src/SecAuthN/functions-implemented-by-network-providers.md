---
description: Die folgenden Funktionen werden von einer Netzwerkanbieter-dll implementiert, um mit dem MultiProvider-Router (MPR) zu kommunizieren.
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Von Netzwerkanbietern implementierte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960548"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="ccd6d-103">Von Netzwerkanbietern implementierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="ccd6d-104">Die folgenden Funktionen werden von einer Netzwerkanbieter-dll implementiert, um mit dem [*MultiProvider-Router*](/windows/desktop/SecGloss/m-gly) (MPR) zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="ccd6d-105">Beachten Sie, dass nur die Funktionen [Funktionen](capabilities-functions.md) von einem Netzwerkanbieter implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="ccd6d-106">Die Implementierung der anderen Arten von Funktionen ist optional und hängt von den Anforderungen des Netzwerk Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="ccd6d-107">Funktions Satz</span><span class="sxs-lookup"><span data-stu-id="ccd6d-107">Function set</span></span>                                                                                    | <span data-ttu-id="ccd6d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccd6d-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccd6d-109">Funktionen-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="ccd6d-110">Ermöglicht dem Aufrufer, die Funktionen des Netzwerk Anbieters zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="ccd6d-111">Benutzernamen Funktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="ccd6d-112">Fordert den Netzwerkanbieter zum Benutzernamen an, der einer Verbindung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="ccd6d-113">Funktionen zum Umleiten von Geräten</span><span class="sxs-lookup"><span data-stu-id="ccd6d-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="ccd6d-114">Ermöglicht einem Netzwerkanbieter das Umleiten von Geräten, Laufwerk Buchstaben und LPT-Ports, die auf dem Microsoft MS-DOS-Betriebssystem standardmäßig sind.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="ccd6d-115">Anbieterspezifische Dialog Feld Funktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="ccd6d-116">Ermöglicht es einem Netzwerkanbieter, Netzwerk spezifische Informationen anzuzeigen oder darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="ccd6d-117">Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="ccd6d-118">Ermöglicht es einem Netzwerkanbieter, spezielle Netzwerk Verzeichnisse anzuzeigen oder darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="ccd6d-119">Enumerationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ccd6d-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="ccd6d-120">Ermöglicht dem Benutzer das Durchsuchen von Netzwerkressourcen.</span><span class="sxs-lookup"><span data-stu-id="ccd6d-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="ccd6d-121">Weitere Informationen zum Erstellen und Registrieren eines Netzwerk Anbieters finden Sie unter [Implementieren eines Netzwerk Anbieters](implementing-a-network-provider.md) und Registrieren von [Netzwerkanbietern und Anmelde Informations Managern](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="ccd6d-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

