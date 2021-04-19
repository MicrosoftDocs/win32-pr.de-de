---
description: Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informationen zur Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346952"
---
# <a name="about-memory-management"></a>Informationen zur Speicherverwaltung

Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht. Jeder Prozess auf 64-Bit-Windows verfügt über einen virtuellen Adressraum von 8 Terabyte. Alle Threads eines Prozesses können auf den virtuellen Adressraum zugreifen. Threads können jedoch nicht auf den Arbeitsspeicher zugreifen, der zu einem anderen Prozess gehört, wodurch verhindert wird, dass ein Prozess von einem anderen Prozess beschädigt wird.

Informationen zum virtuellen Adressraum und den Speicherverwaltungsfunktionen finden Sie in den folgenden Themen.

-   [Virtueller Adressraum](virtual-address-space.md)
-   [Speicher Pools](memory-pools.md)
-   [Informationen zur Speicherleistung](memory-performance-information.md)
-   [Funktionen des virtuellen Arbeitsspeichers](virtual-memory-functions.md)
-   [Heap Funktionen](heap-functions.md)
-   [Datei Zuordnung](file-mapping.md)
-   [Unterstützung großer Arbeitsspeicher](large-memory-support.md)
-   [Globale und lokale Funktionen](global-and-local-functions.md)
-   [Standard-C-Bibliotheksfunktionen](standard-c-library-functions.md)
-   [Vergleichen von Speicher Belegungs Methoden](comparing-memory-allocation-methods.md)

 

 



