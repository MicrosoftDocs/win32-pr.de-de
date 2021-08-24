---
description: Hardwareanbieter implementieren die Schnittstellen IVssProviderCreateSnapshotSet und IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Entwickeln von VSS-Hardwareanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032710"
---
# <a name="developing-vss-hardware-providers"></a>Entwickeln von VSS-Hardwareanbietern

Hardwareanbieter implementieren die Schnittstellen [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) und [**IVssHardwareSnapshotProvider.**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) **IVssProviderCreateSnapshotSet** implementiert die Sequenzierung des Schattenkopiezustands. **IVssHardwareSnapshotProvider** arbeitet mit einer LUN-Abstraktion. Anbieter müssen als out-of-process-COM-Server implementiert werden. Anbieter verwenden anbieterspezifische Mechanismen (häufig private IOCTLs), um mit dem Speichersubsystem zu kommunizieren, das die Schattenkopie-LUNs instanziiert.

-   [Registrierung und Laden des Schattenkopieanbieters](shadow-copy-provider-registration-and-loading.md)
-   [Schattenkopieerstellung für Anbieter](shadow-copy-creation-for-providers.md)
-   [Interaktionen und Verhalten von Hardwareanbietern](hardware-provider-interactions-and-behaviors.md)

 

 



