---
description: Der Leistungsindikatorenanbieter ist ein Hochleistungs Anbieter, der Rohdaten des Leistungs Zählers für die von Win32 perfrawdata abgeleiteten Klassen von WMI-Leistungs Zählern bereitstellt \_ . Der \_ \_ Win32Provider-Instanzname ist &\# 0034; NT5 \_ genericperfprovider \_ v1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Leistungsindikator-Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050469"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="0aca7-104">Leistungsindikator-Provider</span><span class="sxs-lookup"><span data-stu-id="0aca7-104">Performance Counter Provider</span></span>

<span data-ttu-id="0aca7-105">\[Der Leistungsindikatorenanbieter ist nicht mehr zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0aca7-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="0aca7-106">Verwenden Sie stattdessen den [wmiperfinst](wmiperfinst-provider.md) -Anbieter.\]</span><span class="sxs-lookup"><span data-stu-id="0aca7-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="0aca7-107">Der Leistungsindikatorenanbieter ist ein Hochleistungs Anbieter, der Rohdaten des Leistungs Zählers für die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleiteten Klassen von WMI- [Leistungs Zählern](/windows/desktop/CIMWin32Prov/performance-counter-classes) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0aca7-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="0aca7-108">Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname lautet "NT5 \_ genericperfprovider \_ v1".</span><span class="sxs-lookup"><span data-stu-id="0aca7-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="0aca7-109">Die [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen befinden sich im WMI- \\ Namespace "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="0aca7-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="0aca7-110">Jede WMI-Leistungsklasse entspricht einem Leistungs Objekt in einer Leistungs Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="0aca7-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="0aca7-111">Die Eigenschaften dieser Klassen stellen die Leistungsindikatoren für das-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="0aca7-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="0aca7-112">Der WMI-Klassenname für ein unformatierte Counter-Objekt hat das Format \**Win32 \_ \_ \_ perfrawdata* Service \_ Name *\_* Object \_ Name \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="0aca7-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="0aca7-113">Der WMI-Klassenname, der die Leistungsindikatoren für logische Datenträger enthält, lautet beispielsweise [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="0aca7-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="0aca7-114">Sie können die entsprechende [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klasse verwenden, um die im [*System Monitor*](gloss-s.md)angezeigten vorab berechneten Leistungsdaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0aca7-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="0aca7-115">Verwenden Sie z. b. die [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse, um vorab berechnete Datenträger Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0aca7-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="0aca7-116">Weitere Informationen zum Schreiben eines Clients, der auf rohleistungs Daten zugreifen kann, finden Sie unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="0aca7-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="0aca7-117">Als Hochleistungs Anbieter implementiert der Leistungsindikatorenanbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode und die folgenden [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="0aca7-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="0aca7-118">**"Kreaterefreshableaufzählung"**</span><span class="sxs-lookup"><span data-stu-id="0aca7-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="0aca7-119">**"Kreaterefreshableobject"**</span><span class="sxs-lookup"><span data-stu-id="0aca7-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="0aca7-120">**Anmelde Fresher**</span><span class="sxs-lookup"><span data-stu-id="0aca7-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="0aca7-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="0aca7-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="0aca7-122">**Queryinstance**</span><span class="sxs-lookup"><span data-stu-id="0aca7-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="0aca7-123">**Stopp Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="0aca7-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="0aca7-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0aca7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aca7-125">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="0aca7-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
