---
description: Hardware Anbieter implementieren die ivssproviderkreatesnapshotset-und ivsshardwaresnapshotprovider-Schnittstellen.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Entwickeln von VSS-Hardware Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218323"
---
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="9b0be-103">Entwickeln von VSS-Hardware Anbietern</span><span class="sxs-lookup"><span data-stu-id="9b0be-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="9b0be-104">Hardware Anbieter implementieren die [**ivssproviderkreatesnapshotset**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) -und [**ivsshardwaresnapshotprovider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9b0be-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="9b0be-105">**Ivssproviderkreatesnapshotset** implementiert die Status Sequenzierung des Schatten Kopierens.</span><span class="sxs-lookup"><span data-stu-id="9b0be-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="9b0be-106">**Ivsshardwaresnapshotprovider** arbeitet auf einer LUN-Abstraktion.</span><span class="sxs-lookup"><span data-stu-id="9b0be-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="9b0be-107">Anbieter müssen als Prozess interner com-Server implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b0be-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="9b0be-108">Anbieter verwenden anbieterspezifische Mechanismen (oftmals private IOCTLs) für die Kommunikation mit dem Speichersubsystem, das die schattenkopieluns instanziiert.</span><span class="sxs-lookup"><span data-stu-id="9b0be-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="9b0be-109">Registrierung und Laden von schattenkopieanbietern</span><span class="sxs-lookup"><span data-stu-id="9b0be-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="9b0be-110">Erstellen von Schatten Kopien für Anbieter</span><span class="sxs-lookup"><span data-stu-id="9b0be-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="9b0be-111">Interaktionen und Verhalten von Hardware Anbietern</span><span class="sxs-lookup"><span data-stu-id="9b0be-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



