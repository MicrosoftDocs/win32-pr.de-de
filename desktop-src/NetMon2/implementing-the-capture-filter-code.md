---
description: Nachdem Sie festgelegt haben, wie der Filter durch eine capturefilter-Struktur organisiert werden soll, müssen Sie die Struktur zuordnen und ausfüllen, die dann über einen konfigurationsblob an den Netzwerkmonitor-Treiber weitergeleitet wird.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementieren des Erfassungs Filter Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869240"
---
# <a name="implementing-the-capture-filter-code"></a><span data-ttu-id="e37b0-103">Implementieren des Erfassungs Filter Codes</span><span class="sxs-lookup"><span data-stu-id="e37b0-103">Implementing the Capture Filter Code</span></span>

<span data-ttu-id="e37b0-104">Nachdem Sie festgelegt haben, wie der Filter durch eine [**capturefilter**](capturefilter.md) -Struktur organisiert werden soll, müssen Sie die Struktur zuordnen und ausfüllen, die dann über einen konfigurationsblob an den Netzwerkmonitor-Treiber weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e37b0-104">After you determine how to organize your filter through a [**CAPTUREFILTER**](capturefilter.md) structure, you must allocate and fill in the structure, which is then passed to the Network Monitor driver through a configuration BLOB.</span></span>

<span data-ttu-id="e37b0-105">Direkte NPP-Benutzer fügen dem Konfigurations-BLOB den Erfassungs Filter hinzu, der an **Connect**, [**configure**](configure.md)oder Both weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e37b0-105">Direct NPP users add the capture filter to the configuration BLOB that is passed to **Connect**, [**Configure**](configure.md), or both.</span></span> <span data-ttu-id="e37b0-106">Eine Liste der COM-Schnittstellen, die Sie für die Kommunikation mit dem NPP verwenden können, finden Sie unter [NPP-Schnittstellen](npp-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e37b0-106">For a list of COM interfaces that you can use to communicate with the NPP, see [NPP Interfaces](npp-interfaces.md).</span></span>

 

 



