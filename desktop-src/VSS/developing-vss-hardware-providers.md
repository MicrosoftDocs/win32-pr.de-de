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
# <a name="developing-vss-hardware-providers"></a>Entwickeln von VSS-Hardware Anbietern

Hardware Anbieter implementieren die [**ivssproviderkreatesnapshotset**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) -und [**ivsshardwaresnapshotprovider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) -Schnittstellen. **Ivssproviderkreatesnapshotset** implementiert die Status Sequenzierung des Schatten Kopierens. **Ivsshardwaresnapshotprovider** arbeitet auf einer LUN-Abstraktion. Anbieter müssen als Prozess interner com-Server implementiert werden. Anbieter verwenden anbieterspezifische Mechanismen (oftmals private IOCTLs) für die Kommunikation mit dem Speichersubsystem, das die schattenkopieluns instanziiert.

-   [Registrierung und Laden von schattenkopieanbietern](shadow-copy-provider-registration-and-loading.md)
-   [Erstellen von Schatten Kopien für Anbieter](shadow-copy-creation-for-providers.md)
-   [Interaktionen und Verhalten von Hardware Anbietern](hardware-provider-interactions-and-behaviors.md)

 

 



