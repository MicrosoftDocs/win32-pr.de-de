---
title: Bewährte Methoden (Windows-Filter Plattform)
description: In der folgenden Liste finden Sie bewährte Methoden für die Entwicklung von Anwendungen mithilfe der Windows-Filter Plattform (WFP)-API.
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517288"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="7e4a4-103">Bewährte Methoden (Windows-Filter Plattform)</span><span class="sxs-lookup"><span data-stu-id="7e4a4-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="7e4a4-104">In der folgenden Liste finden Sie bewährte Methoden für die Entwicklung von Anwendungen mithilfe der Windows-Filter Plattform (WFP)-API.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="7e4a4-105">Dynamische Sitzungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="7e4a4-106">Viele Anwendungen fügen beim Start Filter Richtlinien Objekte hinzu und löschen diese Objekte dann beim Ende.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="7e4a4-107">Durch die Verwendung einer dynamischen Sitzung garantieren Sie, dass diese Objekte auch dann gelöscht werden, wenn die Anwendung abstürzt.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="7e4a4-108">Außerdem ist das einfache Schließen des Engine-Handles am Ende effizienter, als einzelne Aufrufe zum Löschen der einzelnen Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="7e4a4-109">Behandeln Sie Transaktions Timeouts ordnungsgemäß, oder legen Sie die Sitzungs- **txnwaittimeoutinmsec** auf unendlich fest, um Timeouts zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="7e4a4-110">Auch wenn Sie keine expliziten Transaktionen verwenden, werden die meisten Aufrufe weiterhin unter einer impliziten Transaktion ausgeführt, sodass ein Timeout möglich ist.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="7e4a4-111">Verwenden Sie explizite Transaktionen, um verwandte Add-oder DELETE-Vorgänge in einer einzelnen Transaktion zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="7e4a4-112">Dies ist effizienter und erleichtert das Bereinigen von partiellen Ergebnissen in Fehler Pfaden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="7e4a4-113">Verwenden Sie MUI-kompatible Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="7e4a4-114">Alle lokalisierbaren Zeichen folgen werden in einer gemeinsamen Datenstruktur gespeichert: [**swpm- \_ Anzeige \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="7e4a4-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="7e4a4-115">Die Zeichen folgen in dieser Struktur können indirekte Zeichen Folgen des Typs sein, der von [**shloadderetstring**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="7e4a4-116">Bevor eine **fwpm- \_ Anzeige \_ DATA0** -Struktur von einer der Funktionen zurückgegeben wird, werden die indirekten Zeichen folgen mithilfe des Gebiets Schemas des Aufrufers in die angegebene Zeichen folgen Ressource aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="7e4a4-117">Ordnen Sie alle Objekte einem Anbieter zu.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="7e4a4-118">Wenn mehrere Anbieter auf dem System installiert sind, ist es für Diagnosetools einfacher, festzustellen, wer was hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="7e4a4-119">Fügen Sie Ihrer eigenen Unterschicht Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="7e4a4-120">Sobald ein Beendender Filter in einer untergeordneten Ebene gedrückt wird, werden keine weiteren Filter in dieser Unterschicht ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="7e4a4-121">Wenn Sie also die Filter der gleichen Unterschicht wie ein anderer Anbieter hinzufügen, können Sie verhindern, dass die Filter des anderen aufgerufen werden, was zu unerwarteten Ergebnissen führt.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="7e4a4-122">Verwenden Sie anstelle der Paket orientierten Filterung die Anwendungsschicht-Erzwingung (ALE).</span><span class="sxs-lookup"><span data-stu-id="7e4a4-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="7e4a4-123">Das Filtern auf Paketebene ist langsam.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="7e4a4-124">Filtern Sie ICMP-Fehler und RST-Ereignisse, bevor Sie generiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="7e4a4-125">Dies ist effizienter, wenn diese Ereignisse gefiltert werden, nachdem Sie generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="7e4a4-126">Führen Sie die Paketüberprüfung in der Stream/Datagramm-Datenschicht statt auf der Transport Ebene durch.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="7e4a4-127">Dies gilt für die Entwicklung von Legenden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-127">This applies to developing callouts.</span></span> <span data-ttu-id="7e4a4-128">Weitere Informationen finden Sie unter [Überlegungen zur Programmierung von Legenden Treibern](/windows-hardware/drivers/network/callout-driver-programming-considerations) im Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="7e4a4-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="7e4a4-129">Beachten Sie bei der Verwendung komplexer Filter Auswirkungen auf die Leistung.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="7e4a4-130">Ab Windows 7 und Windows Server 2008 R2 können Filter mit mehreren Bedingungen erstellt werden, die denselben Feld Schlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="7e4a4-131">Dadurch können komplexe Richtlinien mit weniger Filtern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="7e4a4-132">Solche komplexen Filter können jedoch eine langsamere Leistung verursachen, damit das WFP-Filtermodul klassifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="7e4a4-133">Es sollte eine Auswertung vorgenommen werden, um zu bestimmen, ob die Verwendung solcher Filter eine negative Auswirkung auf die Gesamtleistung der Lösung verursacht.</span><span class="sxs-lookup"><span data-stu-id="7e4a4-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
