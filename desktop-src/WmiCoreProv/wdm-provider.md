---
description: Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753712"
---
# <a name="wdm-provider"></a><span data-ttu-id="40ff9-103">WDM-Anbieter</span><span class="sxs-lookup"><span data-stu-id="40ff9-103">WDM Provider</span></span>

<span data-ttu-id="40ff9-104">Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="40ff9-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="40ff9-105">Die Klassen für Hardwaretreiber befinden sich im "root \\ WMI-Namespace".</span><span class="sxs-lookup"><span data-stu-id="40ff9-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="40ff9-106">WDM-Klassen werden primär in "WMI. mof" definiert.</span><span class="sxs-lookup"><span data-stu-id="40ff9-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="40ff9-107">WDM ist eine Betriebssystem Schnittstelle, über die Hardwarekomponenten Informationen und Ereignis Benachrichtigungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="40ff9-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="40ff9-108">Der WDM-Anbieter ist eine Klasse, eine Instanz, ein Ereignis und ein Methoden Anbieter, die Verwaltungs Anwendungen den Zugriff auf Daten und Ereignisse von WMI-for-WDM-fähigen Gerätetreibern ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="40ff9-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="40ff9-109">Die Klassen, die vom WDM-Anbieter zur Darstellung von Gerätetreiber Daten erstellt werden, befinden sich nur im \\ Namespace "root WMI".</span><span class="sxs-lookup"><span data-stu-id="40ff9-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="40ff9-110">Dieser Namespace muss bereits vorhanden sein, bevor der WDM-Anbieter die installierten WDM-Treiber verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40ff9-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="40ff9-111">Der WDM-Anbieter zeichnet Informationen zu WDM-Vorgängen in der Datei wmiprov. log auf.</span><span class="sxs-lookup"><span data-stu-id="40ff9-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="40ff9-112">Weitere Informationen finden Sie unter [WMI-Protokolldateien](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="40ff9-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="40ff9-113">Als Klasse, Instanz, Methode und Ereignis Anbieter implementiert der WDM-Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die folgenden [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="40ff9-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="40ff9-114">**"Kreateclassen"-Sequenz**</span><span class="sxs-lookup"><span data-stu-id="40ff9-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="40ff9-115">**"Kreateingestanceenumasync"**</span><span class="sxs-lookup"><span data-stu-id="40ff9-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="40ff9-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="40ff9-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="40ff9-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="40ff9-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="40ff9-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="40ff9-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="40ff9-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="40ff9-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="40ff9-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="40ff9-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="40ff9-121">Der WDM-Anbieter unterstützt das [**wmievent**](/windows/desktop/WmiCoreProv/wmievent) -System externe-Ereignis, das WMI über Ereignisse von WDM-basierten Treibern benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="40ff9-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="40ff9-122">Sie können Ihre Ereignisconsumer für **wmievent** -Ereignisse wie jedes andere Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="40ff9-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="40ff9-123">Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="40ff9-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="40ff9-124">Beim Starten eines Treibers werden keine Klassen Erstellungs Ereignisse ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="40ff9-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="40ff9-125">Der WDM-Anbieter unterstützt die folgende Klasse:</span><span class="sxs-lookup"><span data-stu-id="40ff9-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="40ff9-126">**Wmibinarymufresource**</span><span class="sxs-lookup"><span data-stu-id="40ff9-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="40ff9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40ff9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ff9-128">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="40ff9-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="40ff9-129">Zugreifen auf Daten von Gerätetreibern</span><span class="sxs-lookup"><span data-stu-id="40ff9-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
