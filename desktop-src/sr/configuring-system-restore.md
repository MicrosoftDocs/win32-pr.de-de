---
title: Konfigurieren der System Wiederherstellung
description: Die System Wiederherstellung verwendet Windows-Verwaltungsinstrumentation (WMI), um eine Skript fähige Methode zum Konfigurieren und Verwenden der Funktionalität bereitzustellen. Es macht zwei Klassen (SystemRestore und systemrestoreconfig) im Stamm- \\ Standard Namespace verfügbar.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390556"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="9b2f3-104">Konfigurieren der System Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="9b2f3-104">Configuring System Restore</span></span>

<span data-ttu-id="9b2f3-105">Die System Wiederherstellung verwendet [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI), um eine Skript fähige Methode zum Konfigurieren und Verwenden der Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b2f3-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="9b2f3-106">Es macht zwei Klassen ( [**SystemRestore**](systemrestore.md) und [**systemrestoreconfig**](systemrestoreconfig.md)) im Stamm- \\ Standard Namespace verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b2f3-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="9b2f3-107">Die [**SystemRestore**](systemrestore.md) -Klasse bietet Methoden für die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="9b2f3-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="9b2f3-108">Deaktivieren und Aktivieren der Überwachung</span><span class="sxs-lookup"><span data-stu-id="9b2f3-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="9b2f3-109">Auflisten verfügbarer Wiederherstellungspunkte</span><span class="sxs-lookup"><span data-stu-id="9b2f3-109">Listing available restore points</span></span>
-   <span data-ttu-id="9b2f3-110">Initiieren einer Wiederherstellung auf dem lokalen System</span><span class="sxs-lookup"><span data-stu-id="9b2f3-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="9b2f3-111">Abrufen des Status der letzten Systemwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="9b2f3-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="9b2f3-112">Die [**systemrestoreconfig**](systemrestoreconfig.md) -Klasse stellt Eigenschaften zum Steuern der Häufigkeit der geplanten Wiederherstellungspunkt Erstellung und des Speicherplatzes bereit, der von der System Wiederherstellung auf jedem Laufwerk beansprucht wird.</span><span class="sxs-lookup"><span data-stu-id="9b2f3-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="9b2f3-113">Auf beide Klassen kann mithilfe von standardmäßigen WMI-Techniken Remote zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9b2f3-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="9b2f3-114">Eine umfassende Beschreibung von WMI finden Sie unter [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="9b2f3-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 