---
description: Client Anwendungen und Skripts, die auf standardmäßige WMI-32-Bit-Anbieter zugreifen, funktionieren bei Ausführung unter einem 64-Bit-Betriebssystem weiterhin normal.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569921"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="60142-103">Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer</span><span class="sxs-lookup"><span data-stu-id="60142-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="60142-104">Client Anwendungen und Skripts, die auf standardmäßige WMI-32-Bit-Anbieter zugreifen, funktionieren bei Ausführung unter einem 64-Bit-Betriebssystem weiterhin normal.</span><span class="sxs-lookup"><span data-stu-id="60142-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="60142-105">Nur zwei vorinstallierte Anbieter, der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) und der [Ansichts Anbieter](view-provider.md), haben 64-Bit-Versionen, die mit den 32-Bit-Versionen parallel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60142-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="60142-106">Eine 32-Bit-Anwendung, die 32-Bit-Windows-Treibermodell-Instanzen (WDM) anfordert, empfängt jedoch die standardmäßigen 64-Bit-WDM-Klassen Instanzen auf einem 64-Bit-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="60142-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="60142-107">Zugreifen auf Standard-und nicht standardmäßige Anbieter Daten</span><span class="sxs-lookup"><span data-stu-id="60142-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="60142-108">Im Allgemeinen enthalten Anbieterwriter nicht sowohl 32-Bit-als auch 64-Bit-Versionen eines Anbieters im gleichen Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="60142-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="60142-109">Wenn kein 64-Bit-Anbieter vorhanden ist, kann ein 32-Bit-Anbieter weiterhin über die Funktionen von WOW64 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60142-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="60142-110">Ein 64-Bit-Anbieter kann auch Daten für eine 32-Bit-Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="60142-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="60142-111">Weitere Informationen finden Sie unter [Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="60142-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="60142-112">Wenn zwei Versionen vorhanden sind, können Client Anwendungen und Skripts die in der com- [API](com-api-for-wmi.md) verfügbaren Kontext Parameter und die [Skript-API](scripting-api-for-wmi.md) verwenden, um eine explizite Verbindung mit einem bestimmten nicht standardmäßigen WMI-Anbieter herzustellen, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60142-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="60142-113">Weitere Informationen finden Sie unter [anfordern von WMI-Daten auf einer 64-Bit-Plattform](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="60142-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="60142-114">Das folgende Diagramm zeigt die standardmäßigen und nicht standardmäßigen Verbindungen, wobei die Registrierung als Beispiel verwendet wird, für das zwei Anbieter nebeneinander auf einer 64-Bit-Plattform vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="60142-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![Standard-und nicht standardmäßige Verbindungen auf einer 64-Bit-Plattform](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="60142-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60142-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60142-117">Anfordern von WMI-Daten auf einer 64-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="60142-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="60142-118">Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="60142-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
