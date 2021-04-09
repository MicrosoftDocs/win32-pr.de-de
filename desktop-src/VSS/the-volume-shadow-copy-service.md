---
description: Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen bereit.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Der Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751601"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="ba93c-103">Der Volumeschattenkopie-Dienst</span><span class="sxs-lookup"><span data-stu-id="ba93c-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="ba93c-104">Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen bereit.</span><span class="sxs-lookup"><span data-stu-id="ba93c-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="ba93c-105">VSS ist zwar größtenteils für Benutzer und Entwickler transparent, doch führt VSS Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="ba93c-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="ba93c-106">Koordiniert Aktivitäten von Anbietern, Writern und Anforderern bei der Erstellung und Verwendung von Schatten Kopien.</span><span class="sxs-lookup"><span data-stu-id="ba93c-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="ba93c-107">Gibt den Standardsystem Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="ba93c-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="ba93c-108">Implementiert die Treiber Funktionalität auf niedriger Ebene, die für jeden Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ba93c-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="ba93c-109">Der VSS-Dienst startet on demand. Dies bedeutet, dass dieser Dienst erst aktiviert werden muss, damit VSS-Vorgänge ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba93c-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



