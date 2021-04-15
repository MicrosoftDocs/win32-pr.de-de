---
description: Ein Netzwerk wird als Transportmechanismus angezeigt, der Daten von einem Punkt an einen anderen überträgt.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485315"
---
# <a name="network"></a><span data-ttu-id="966cd-103">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="966cd-103">Network</span></span>

<span data-ttu-id="966cd-104">Ein Netzwerk wird als Transportmechanismus angezeigt, der Daten von einem Punkt an einen anderen überträgt.</span><span class="sxs-lookup"><span data-stu-id="966cd-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="966cd-105">TAPI-Dienstanbieter behandeln die spezifischen Protokolle, die zum Ausführen von Vorgängen erforderlich sind, z. b. das Einrichten einer Kommunikationssitzung in einem bestimmten</span><span class="sxs-lookup"><span data-stu-id="966cd-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="966cd-106">Eine Endbenutzer-oder Serveranwendung benötigt normalerweise nur sehr allgemeine Netzwerkinformationen, wie z. b. adreetstyp.</span><span class="sxs-lookup"><span data-stu-id="966cd-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="966cd-107">Einige allgemeine Arten von Netzwerken:</span><span class="sxs-lookup"><span data-stu-id="966cd-107">Some common types of networks:</span></span>

-   <span data-ttu-id="966cd-108">**Pots (Plain Old Telefon Service):** Die Sprache und die Daten werden im analogen Format in der *lokalen Schleife* übertragen und an anderer Stelle Digital übertragen.</span><span class="sxs-lookup"><span data-stu-id="966cd-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="966cd-109">In der Regel wird ein Medientyp pro Rückruf, ein Kanal pro Zeile, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="966cd-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="966cd-110">**ISDN (digitales Service Digital Network):** Digital übertragen.</span><span class="sxs-lookup"><span data-stu-id="966cd-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="966cd-111">Geschwindigkeiten von bis zu 128 Kbit/s für BRI-ISDN-Linien (Basic Rate Interface) und viel höher in den PRI-ISDN-Linien (Primary Rate Interface).</span><span class="sxs-lookup"><span data-stu-id="966cd-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="966cd-112">Mindestens drei Kanäle und so viele 32-Kanäle für die gleichzeitige, unabhängige Übertragung von Sprache und Daten.</span><span class="sxs-lookup"><span data-stu-id="966cd-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="966cd-113">Internationaler Standard.</span><span class="sxs-lookup"><span data-stu-id="966cd-113">International standard.</span></span>
-   <span data-ttu-id="966cd-114">**T1/E1:** Digital übertragen.</span><span class="sxs-lookup"><span data-stu-id="966cd-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="966cd-115">T1 ist eine Übertragungs Verbindung mit einer Kapazität von 1,544 Mbit/s, die in der Regel zum Verbinden von Netzwerken über Remote Abstände verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="966cd-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="966cd-116">In der Europäischen Union wird T1 als E1 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="966cd-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="966cd-117">**56 gewechselt:** Signalisieren von 56 Kbit/s über einwähltelefonleitungen, erfordert jedoch spezielle Geräte.</span><span class="sxs-lookup"><span data-stu-id="966cd-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="966cd-118">Beschränkt auf Aufrufe von anderen speziell ausgestatteten Einrichtungen.</span><span class="sxs-lookup"><span data-stu-id="966cd-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="966cd-119">**Centrex:** Zentralisierte Netzwerkdienste über reguläre Telefonleitungen und Geräte mit Telefonunternehmen.</span><span class="sxs-lookup"><span data-stu-id="966cd-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="966cd-120">Es sind keine speziellen Geräte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="966cd-120">No special equipment required.</span></span>
-   <span data-ttu-id="966cd-121">**Digitaler PBXs-Austausch (privater Zweig Austausch) und Schlüsselsysteme:** Sprach-und Datenübertragung auf privaten Telefonsystemen mithilfe von proprietären Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="966cd-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="966cd-122">**IP-Netzwerke:** Sprache und Daten, die in Netzwerken über das Internetprotokoll (IP) übertragen werden, z. b. das Internet selbst oder ein Unternehmens Intranet.</span><span class="sxs-lookup"><span data-stu-id="966cd-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="966cd-123">Diese Liste enthält nicht alle Komponenten.</span><span class="sxs-lookup"><span data-stu-id="966cd-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="966cd-124">Jeder Netzwerk Transportmechanismus kann unter Berücksichtigung geeigneter Dienstanbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="966cd-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



