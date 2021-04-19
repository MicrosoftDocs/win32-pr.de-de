---
description: Ein Dienst, Treiber oder eine Anwendung, der gegen Daten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Bereitstellen von Leistungsdaten mit Leistungs-dll
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356166"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="4d6e3-103">Bereitstellen von Leistungsdaten mit Leistungs-dll</span><span class="sxs-lookup"><span data-stu-id="4d6e3-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d6e3-104">Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="4d6e3-105">Stattdessen empfiehlt Microsoft die Verwendung der Methode, die unter [Bereitstellen von Indikator Daten mithilfe von Version 2,0](providing-counter-data-using-version-2-0.md) zum Erstellen neuer Leistungsindikatoren beschrieben wird. Außerdem empfiehlt es sich, vorhandene Leistungsindikatoren zu migrieren, um auch diese Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="4d6e3-106">Ein Dienst, Treiber oder eine Anwendung, der gegen Daten bereitstellen möchte, kann eine Leistungs-DLL schreiben, um die Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="4d6e3-107">Wenn ein Consumer Leistungsdaten abfragt, lädt das System die Anbieter-DLL in den Prozess des Consumers und ruft den Anbieter auf, um die Daten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="4d6e3-108">Ausführliche Informationen zum Schreiben der Leistungs-dll finden Sie unter [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md).</span><span class="sxs-lookup"><span data-stu-id="4d6e3-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="4d6e3-109">Das System verwendet die Registrierung, um zu bestimmen, welcher Anbieter aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="4d6e3-110">Informationen zum Registrieren Ihres Anbieters und der von ihm unterstützten Leistungsindikatoren finden Sie unter [Hinzufügen von Leistungsindikatoren](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="4d6e3-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="4d6e3-111">Leistungs-DLLs werden von Windows onecore nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="4d6e3-112">Wenn Sie eine Komponente schreiben, die unter Windows onecore ausgeführt werden muss, verwenden Sie die unter [Bereitstellen von Counter-Daten mithilfe von Version 2,0](providing-counter-data-using-version-2-0.md)beschriebene Methode.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
