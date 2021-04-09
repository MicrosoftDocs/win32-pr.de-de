---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960733"
---
# <a name="p-wmi"></a><span data-ttu-id="dc0ea-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="dc0ea-103">P (WMI)</span></span>

<span data-ttu-id="dc0ea-104">[a](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="dc0ea-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dc0ea-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**Leistungs Zählers**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-106">Eine Eigenschaft in einer Leistungsklasse, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitet ist und Leistungsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**Leistungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-108">Ein Objekt in einer Leistungs Bibliothek, in dem Daten in Leistungsindikatoren gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="dc0ea-109">Diese Objekte sind im [*System Monitor*](gloss-s.md) -Hilfsprogramm sichtbar.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="dc0ea-110">Beispiele hierfür sind Cache-und logische Datenträger Objekte.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="dc0ea-111">Bei der Übertragung in WMI durch den [*ADAP*](gloss-a.md) -Prozess werden die einzelnen Objekte zu zwei WMI-Leistungsklassen.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="dc0ea-112">Eine Klasse, die Rohdaten enthält, wird von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="dc0ea-113">Die andere Klasse wird von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet und enthält die gleichen Daten, die im System Monitor sichtbar sind, wie vom gekochten Leistungsindikatoren-Anbieter berechnet.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**dauerhafter Consumer**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-115">Ein [*Ereignisconsumer*](gloss-e.md) , dessen Registrierung so lange dauert, bis er explizit abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="dc0ea-116">Siehe auch [*temporärer Consumer*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="dc0ea-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physischer Consumer**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-118">Ein COM-Objekt, das von einem [*Ereignisconsumeranbieter*](gloss-e.md) implementiert wird und eine [*Senke*](gloss-s.md) für den Empfang von Ereignis Benachrichtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Property**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-120">Ein Name-Wert-Paar, das eine Dateneinheit für eine Klasse beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="dc0ea-121">Eigenschaftswerte müssen einen gültigen [*Managed Object Format (MOF)*](gloss-m.md) -Datentyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="dc0ea-122">Siehe auch [*Reference-Eigenschaft*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="dc0ea-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**Eigenschaften Anbieter**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-124">Ein com-Server, der das Abrufen und Ändern von WMI-Eigenschaften unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="dc0ea-125">Eigenschafts Anbieter implementieren die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -und [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**ab**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-127">Ein com-Server, der mit verwalteten Objekten kommuniziert, um auf Daten und Ereignis Benachrichtigungen wie die Registrierung oder ein SNMP-Gerät zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="dc0ea-128">Anbieter leiten diese Daten zur Integration und Interpretation an die [*CIM-Objekt-Manager*](gloss-c.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ea-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**Provider-Methode**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="dc0ea-130">Eine Methode, die von einem WMI- *Anbieter* implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
