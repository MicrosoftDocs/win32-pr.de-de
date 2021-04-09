---
description: Bei einem Monitor handelt es sich um eine DLL (Dynamic Link Library), die echt Zeiterfassung von Netzwerk Datenverkehr untersucht.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959016"
---
# <a name="monitors"></a><span data-ttu-id="98bb4-103">Monitore</span><span class="sxs-lookup"><span data-stu-id="98bb4-103">Monitors</span></span>

<span data-ttu-id="98bb4-104">Bei einem Monitor handelt es sich um eine DLL (Dynamic Link Library), die echt Zeiterfassung von Netzwerk Datenverkehr untersucht.</span><span class="sxs-lookup"><span data-stu-id="98bb4-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="98bb4-105">Er sucht nach vordefinierten Bedingungen und generiert dann Ereignisse, wenn diese Bedingungen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="98bb4-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="98bb4-106">Beispielsweise kann ein Ereignis ausgelöst werden, wenn versucht wird, einen Netzwerk Umbruch auszuführen, wenn eine nicht autorisierte Arbeitsstation IP-Adressen ausgibt oder wenn ein Router ausfällt.</span><span class="sxs-lookup"><span data-stu-id="98bb4-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="98bb4-107">Wenn Sie detaillierte Analysen der Netzwerkdaten durchführen müssen, die eine nach Erfassungs Analyse erfordern, müssen Sie [*Experten*](e.md) -und [*Parser*](p.md) -Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="98bb4-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="98bb4-108">Der [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) stellt das Framework zum Verwalten Ihrer Monitore bereit.</span><span class="sxs-lookup"><span data-stu-id="98bb4-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="98bb4-109">Es stellt Funktionen zum Laden der Monitor-DLLs und eine Kommunikationsschnittstelle zum Monitor-Steuerungs Tool bereit, sodass Sie mehrere Instanzen Ihrer Monitore erstellen, konfigurieren, starten, Abbrechen und deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="98bb4-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="98bb4-110">Monitore werden in zwei Ausführungs Threads ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98bb4-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="98bb4-111">Mcsvc stellt den ersten Thread bereit, der die direkte Steuerung des Monitors ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="98bb4-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="98bb4-112">Der zweite Thread wird vom [*Netzwerk Paketanbieter*](n.md) (NPP) bereitgestellt, der eine Möglichkeit bietet, die erfassten Netzwerkdaten, Statistiken und den Status der Erfassung von der NPP zurück an den Monitor zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="98bb4-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="98bb4-113">Es können mehr als eine Instanz desselben Monitors für jede Lauf Zeit-NPP-Schnittstelle vorhanden sein, die zum Erfassen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98bb4-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



