---
description: Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: WMI-SNMP-Klassen Korrelation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215442"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="14bc6-103">WMI-SNMP-Klassen Korrelation</span><span class="sxs-lookup"><span data-stu-id="14bc6-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="14bc6-104">Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="14bc6-105">Korrelierte Klassen sind solche, die ein bestimmtes SNMP-Gerät unterstützt, wenn die Enumeration auftritt.</span><span class="sxs-lookup"><span data-stu-id="14bc6-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="14bc6-106">Nicht korrelierte Enumeration gibt alle innerhalb des SMIR vorhandenen Klassen zurück, unabhängig davon, ob Sie vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="14bc6-107">Die Korrelation ist eine Funktion des WMI-SNMP-Anbieters und kann deaktiviert oder aktiviert werden (Standard).</span><span class="sxs-lookup"><span data-stu-id="14bc6-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="14bc6-108">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="14bc6-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="14bc6-109">Mithilfe der Korrelation können alle Klassen angezeigt werden, die tatsächlich von einem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="14bc6-110">Wenn Sie wissen, dass eine bestimmte Klasse unterstützt wird, aber nicht im SMIR angezeigt wird, kann dies auf verschiedene Gründe zurückzuführen sein, von denen eine Korrelation ist.</span><span class="sxs-lookup"><span data-stu-id="14bc6-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="14bc6-111">Sie sollten die Korrelation deaktivieren, bevor Sie auf das betreffende Gerät schreiben.</span><span class="sxs-lookup"><span data-stu-id="14bc6-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="14bc6-112">Das Deaktivieren der Korrelation führt jedoch zu der Wahrscheinlichkeit, dass viele vom Gerät nicht unterstützte Klassen in SMIR angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="14bc6-113">Außerdem entstehen bei der Verwendung der Korrelation Kosten für die Leistung, da das Gerät abgefragt wird, um zu sehen, welche Klassen es unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14bc6-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="14bc6-114">Wenn die Korrelation aktiviert ist, verursacht der SNMP-Anbieter eine Enumeration von Geräten unterstützten Klassen, die dem Ergebnis der Ausführung eines *MIB Walk* -Tools ähneln.</span><span class="sxs-lookup"><span data-stu-id="14bc6-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="14bc6-115">Ein Netzwerk-Manager möchte beispielsweise verschiedene wichtige Daten zu allen verwalteten Hubs in einem bestimmten Netzwerk kennen.</span><span class="sxs-lookup"><span data-stu-id="14bc6-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="14bc6-116">Eine Datenbank der aktuellen Geräte und ihrer unterstützten MISB ist bereits vorhanden, daher besteht keine Notwendigkeit, sich auf die Korrelations Funktion des Geräts zu verlassen, um die unterstützten Datenelemente bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="14bc6-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="14bc6-117">In diesem Fall könnte die Korrelation deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="14bc6-118">Im folgenden Beispiel wird gezeigt, wie die Korrelation deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="14bc6-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="14bc6-119">Andererseits kann ein anderer Netzwerk-Manager alle UNIX-Computer Laufwerke im Netzwerk überwachen, aber nicht mit den MIB-Daten auf diesen Computern vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="14bc6-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="14bc6-120">In diesem Fall würde die Korrelation aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="14bc6-120">In that case, correlation would be turned on.</span></span>

 

 



