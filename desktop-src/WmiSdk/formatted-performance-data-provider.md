---
description: Berechnete Liefer (&\# 0034; gekocht&\# 0034;) Leistungsdaten des Leistungs Zählers. Stellt dynamische Daten für die WMI-Klassen bereit, die von Win32 \_ perfformatteddata abgeleitet werden. Wird auch als gekochte gegen Anbieter bezeichnet.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Formatierte Leistungs Datenanbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360190"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="8b16c-105">Formatierte Leistungs Datenanbieter</span><span class="sxs-lookup"><span data-stu-id="8b16c-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="8b16c-106">\[Die formatierte Leistungs Datenanbieter, auch bekannt als "gekochte Leistungs Anbieter", ist nicht mehr zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b16c-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="8b16c-107">Verwenden Sie stattdessen den [wmiperfinst](wmiperfinst-provider.md) -Anbieter.\]</span><span class="sxs-lookup"><span data-stu-id="8b16c-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="8b16c-108">Der leistungsfähige Hochleistungs Datenanbieter liefert berechnete ("gekochte") Leistungsdaten, z. b. den Prozentsatz der Zeit, die ein Datenträger für das Schreiben von Daten benötigt.</span><span class="sxs-lookup"><span data-stu-id="8b16c-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="8b16c-109">Dieser Anbieter stellt dynamische Daten für die WMI-Klassen bereit, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8b16c-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="8b16c-110">Der Unterschied zwischen diesem Anbieter und dem [Leistungsindikatorenanbieter](performance-counter-provider.md) besteht darin, dass der Leistungsindikatorenanbieter Rohdaten bereitstellt und [](gloss-s.md)der gekochte Leistungsindikatoren Leistungsdaten liefert</span><span class="sxs-lookup"><span data-stu-id="8b16c-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="8b16c-111">Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname ist "hiperfkocher \_ v1".</span><span class="sxs-lookup"><span data-stu-id="8b16c-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="8b16c-112">Der WMI-formatierte Klassenname für ein Counter-Objekt hat die Form "Win32 \_ perfformatteddata \_ *Service \_ Name* \_ *Object \_ Name*".</span><span class="sxs-lookup"><span data-stu-id="8b16c-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="8b16c-113">Der WMI-Klassenname, der die Leistungsindikatoren für logische Datenträger enthält, lautet beispielsweise **Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="8b16c-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="8b16c-114">Diese Klassen befinden sich im \\ Namespace "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="8b16c-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="8b16c-115">Da Leistungsdaten Klassen auf einem bestimmten System dynamisch hinzugefügt und geändert werden, ist es nicht möglich, die Eigenschaften aller bekannten Leistungs Objekte formal zu dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="8b16c-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="8b16c-116">Informationen dazu, welche Klassen für Sie verfügbar sind, und um zu ermitteln, welche Member diese Klassen haben, finden Sie unter [Abrufen der Dokumentation für Rohdaten und formatierte Leistungsdaten Objekte](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="8b16c-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="8b16c-117">Die [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen verwenden den **cookingtype** -Qualifizierer in [WMI-Leistungsdaten Typen](wmi-performance-counter-types.md) , um die Formel für die Berechnung der Leistungsdaten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b16c-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="8b16c-118">Dieser Qualifizierer ist mit dem **CounterType** -Qualifizierer in den [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen identisch.</span><span class="sxs-lookup"><span data-stu-id="8b16c-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="8b16c-119">Als Hochleistungs Anbieter implementiert der gekochte Leistungs Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode und die folgenden [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="8b16c-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="8b16c-120">**"Kreaterefreshableaufzählung"**</span><span class="sxs-lookup"><span data-stu-id="8b16c-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="8b16c-121">**"Kreaterefreshableobject"**</span><span class="sxs-lookup"><span data-stu-id="8b16c-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="8b16c-122">**Anmelde Fresher**</span><span class="sxs-lookup"><span data-stu-id="8b16c-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="8b16c-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="8b16c-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="8b16c-124">**Queryinstance**</span><span class="sxs-lookup"><span data-stu-id="8b16c-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="8b16c-125">**Stopp Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="8b16c-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="8b16c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b16c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b16c-127">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b16c-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
