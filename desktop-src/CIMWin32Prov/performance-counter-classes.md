---
description: Leistungs Bestellungs Klassen erlauben Skript-und Programm Zugriff auf Systemleistungs Daten, die von vorhandenen Hochleistungs Anbietern berechnet werden.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Leistungs Leistungsdaten-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861747"
---
# <a name="performance-counter-classes"></a><span data-ttu-id="c16e7-103">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="c16e7-103">Performance Counter Classes</span></span>

<span data-ttu-id="c16e7-104">Leistungs Bestellungs Klassen erlauben Skript-und Programm Zugriff auf Systemleistungs Daten, die von vorhandenen Hochleistungs Anbietern berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c16e7-104">Performance Counter classes allow script and program access to system performance data calculated by existing high-performance providers.</span></span> <span data-ttu-id="c16e7-105">Diese Klassen bestehen aus reinen Leistungsdaten und formatierten Leistungs Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="c16e7-105">These classes consist of raw performance counter classes and formatted performance counter classes.</span></span>

<span data-ttu-id="c16e7-106">Verschiedene Anbieter stellen Leistungs Bibliotheksdaten über WMI bereit.</span><span class="sxs-lookup"><span data-stu-id="c16e7-106">Different providers supply performance library data through WMI.</span></span> <span data-ttu-id="c16e7-107">Die Anbieter [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) und [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) stellen Klassen für die [Leistungsindikatoren](/windows/desktop/PerfCtrs/performance-counters-portal)Version 1 und Version 2 bereit.</span><span class="sxs-lookup"><span data-stu-id="c16e7-107">The [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) and [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) providers supply classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="c16e7-108">Diese Anbieter gewährleisten die Kompatibilität mit den in früheren Betriebssystemen verfügbaren Klassen.</span><span class="sxs-lookup"><span data-stu-id="c16e7-108">These providers maintain compatibility with the classes available in earlier operating systems.</span></span>

<span data-ttu-id="c16e7-109">Die Klassen in diesem Abschnitt sind die abstrakten Basisklassen, die zum Erstellen von Leistungs Zählers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c16e7-109">The classes in this section are the abstract base classes used to create performance counter classes.</span></span> <span data-ttu-id="c16e7-110">Dies ist keine komplette Liste der Klassen, die Sie möglicherweise auf Ihrem Betriebssystem finden.</span><span class="sxs-lookup"><span data-stu-id="c16e7-110">This is not a complete list of classes that you may find on your operating system.</span></span> <span data-ttu-id="c16e7-111">Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c16e7-111">For more information, see [Performance Libraries and WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c16e7-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c16e7-112">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c16e7-113">**Win32 \_ -Leistung**</span><span class="sxs-lookup"><span data-stu-id="c16e7-113">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dd>

<span data-ttu-id="c16e7-114">Die Basisklasse für die Leistungs Zählers-Klassen [**Win32 \_ perfrawdata**](win32-perfrawdata.md) und [**Win32 \_ perfformatteddata**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="c16e7-114">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

</dd> <dt>

[<span data-ttu-id="c16e7-115">**Win32 \_ perfformatteddata**</span><span class="sxs-lookup"><span data-stu-id="c16e7-115">**Win32\_PerfFormattedData**</span></span>](win32-perfformatteddata.md)
</dt> <dd>

<span data-ttu-id="c16e7-116">eine abstrakte Basisklasse für die vorinstallierten, berechneten Daten Klassen.</span><span class="sxs-lookup"><span data-stu-id="c16e7-116">an abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

[<span data-ttu-id="c16e7-117">**Win32- \_ perfrawdata**</span><span class="sxs-lookup"><span data-stu-id="c16e7-117">**Win32\_PerfRawData**</span></span>](win32-perfrawdata.md)
</dt> <dd>

<span data-ttu-id="c16e7-118">Die abstrakte Basisklasse für alle konkreten Klassen des-rohleistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="c16e7-118">The abstract base class for all concrete raw performance counter classes.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c16e7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c16e7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c16e7-120">Win32-Klassen</span><span class="sxs-lookup"><span data-stu-id="c16e7-120">Win32 Classes</span></span>](win32-provider.md)
</dt> </dl>

 

 
