---
description: Sie können einen Klassen Anbieter als Push-oder Pull-Anbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Bestimmen des Push-oder Pull-Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372977"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="4b7e6-103">Bestimmen des Push-oder Pull-Status</span><span class="sxs-lookup"><span data-stu-id="4b7e6-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="4b7e6-104">Sie können einen Klassen Anbieter als Push-oder Pull-Anbieter modellieren, der angibt, wie ein Anbieter die Interaktion mit WMI erwartet.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="4b7e6-105">Pull-Anbieter empfangen eine Anforderung von WMI und erfüllen die Anforderung, indem Sie die Daten dynamisch erzeugen oder aus einem lokalen Cache abrufen.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="4b7e6-106">Außerdem müssen Pull-Anbieter eine große Anzahl von Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="4b7e6-107">Ein Pull-Anbieter generiert Klassendefinitionen dynamisch.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="4b7e6-108">In der Regel ändern sich die von einem Pull-Anbieter verwalteten Daten häufig, sodass der Anbieter die Klasse dynamisch generieren oder die Klasse aus einem lokalen Cache abrufen kann, wenn eine Anwendung eine Anforderung ausgibt.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="4b7e6-109">Ein Pull-Anbieter muss eigene Datenabruf-, Cache-und Ereignis Benachrichtigungsmechanismen implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="4b7e6-110">Da es sich bei den meisten Anbietern um Pull-Anbieter handelt, wird von der Dokumentation in dieser Datei ausgegangen, dass Sie einen Pull-Anbieter entwickeln, sofern nicht explizit</span><span class="sxs-lookup"><span data-stu-id="4b7e6-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="4b7e6-111">Im Gegensatz dazu verwendet WMI Daten im WMI-Repository, um alle Anwendungsanforderungen für pushanbieter zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="4b7e6-112">Pushanbieter verwenden auch weniger Schnittstellen Methoden und sind daher einfacher zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="4b7e6-113">Ein pushanbieter verwendet das WMI-Repository als Speicherbereich für Informationen über das verwaltete Objekt und aktualisiert diese Informationen nur während der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="4b7e6-114">Beispielsweise wird der WDM-Klassen Anbieter, der im WMI-Abschnitt des Microsoft Windows Software Development Kit (SDK) enthalten ist, als pushanbieter modelliert.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="4b7e6-115">Durch die Verwendung des WMI-Repository als Speicherbereich erhält ein Push-Anbieter die folgenden Vorteile gegenüber einem Pull-Anbieter:</span><span class="sxs-lookup"><span data-stu-id="4b7e6-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="4b7e6-116">Der Anbieter muss keinen lokalen Cache zum Speichern von Daten implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="4b7e6-117">Der Anbieter muss das Abrufen von Daten nicht unterstützen. Stattdessen kann sich der Anbieter auf WMI verlassen, um Abruf Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="4b7e6-118">Wenn eine Anwendung vom Anbieter bereitgestellte Daten anfordert, wird diese Anforderung von WMI erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="4b7e6-119">Der Anbieter kann auch auf WMI zurückgreifen, um die Ereignis Benachrichtigung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="4b7e6-120">Da ein pushanbieter jedoch nur während der Initialisierung aktualisiert wird, werden alle Änderungen an einer Klasse im WMI-Repository einige Zeit nicht wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="4b7e6-121">Aus diesem Grund funktioniert das Push-Anbieter Modell am besten mit Klassen, die sich kaum ändern, oder andere sind vollständig statisch.</span><span class="sxs-lookup"><span data-stu-id="4b7e6-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



