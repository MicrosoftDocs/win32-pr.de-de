---
description: Das Microsoft&\# 160; Der Win32-Anbieter ruft für Windows-Systeme relevante Daten&\# 8212 ab und aktualisiert diese, z. b. die aktuellen Einstellungen der Umgebungsvariablen und die Attribute eines logischen Datenträgers.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Win32-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747904"
---
# <a name="win32-provider"></a><span data-ttu-id="ffa0a-103">Win32-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ffa0a-103">Win32 Provider</span></span>

<span data-ttu-id="ffa0a-104">Der Microsoft Win32-Anbieter ruft für Windows-Systeme relevante Daten ab und aktualisiert Sie – Daten, wie z. b. die aktuellen Einstellungen von Umgebungsvariablen und die Attribute eines logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="ffa0a-105">Mit dem Win32-Anbieter können Verwaltungs Anwendungen WMI für den einfachen Zugriff auf diese Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="ffa0a-106">Der Win32-Anbieter ruft seine Informationen mithilfe von Windows-Funktionsaufrufen und Abfragen der Systemregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="ffa0a-107">Der Win32-Anbieter definiert die Klassen, die zum Beschreiben von Hardware oder Software auf Windows-Systemen und deren Beziehungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="ffa0a-108">Als Instanz-und Methoden Anbieter implementiert der Win32-Anbieter die standardmäßige [**iwbemproviderinit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die folgenden [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="ffa0a-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="ffa0a-109">**"Kreateingestanceenumasync"**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="ffa0a-110">**Delta einstanceasync**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="ffa0a-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="ffa0a-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="ffa0a-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="ffa0a-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="ffa0a-115">In der folgenden Tabelle sind die Kategorien der Win32-Anbieter Klassen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="ffa0a-116">Klassen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-116">Classes</span></span>                                                                             | <span data-ttu-id="ffa0a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffa0a-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="ffa0a-118">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="ffa0a-119">Hardware bezogene Objekte.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="ffa0a-120">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="ffa0a-121">Mit dem Betriebssystem verbundene Objekte.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="ffa0a-122">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="ffa0a-123">Rohdaten und berechnete Leistungsdaten aus Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="ffa0a-124">WMI-Dienst Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="ffa0a-125">Verwaltung für WMI.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ffa0a-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ffa0a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa0a-127">Cimwin32-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ffa0a-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
