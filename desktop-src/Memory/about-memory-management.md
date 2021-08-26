---
description: Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informationen zur Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869970"
---
# <a name="about-memory-management"></a>Informationen zur Speicherverwaltung

Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht. Jeder Prozess auf 64-Bit-Windows hat einen virtuellen Adressraum von 8 Terabyte. Alle Threads eines Prozesses können auf seinen virtuellen Adressraum zugreifen. Threads können jedoch nicht auf Arbeitsspeicher zugreifen, der zu einem anderen Prozess gehört, wodurch ein Prozess vor einer Beschädigung durch einen anderen Prozess geschützt wird.

Informationen zum virtuellen Adressraum und den Speicherverwaltungsfunktionen finden Sie in den folgenden Themen.

-   [Virtueller Adressraum](virtual-address-space.md)
-   [Speicherpools](memory-pools.md)
-   [Arbeitsspeicherleistungsinformationen](memory-performance-information.md)
-   [Funktionen des virtuellen Arbeitsspeichers](virtual-memory-functions.md)
-   [Heapfunktionen](heap-functions.md)
-   [Dateizuordnung](file-mapping.md)
-   [Unterstützung für großen Arbeitsspeicher](large-memory-support.md)
-   [Globale und lokale Funktionen](global-and-local-functions.md)
-   [C-Standardbibliotheksfunktionen](standard-c-library-functions.md)
-   [Vergleichen von Speicherzuordnungsmethoden](comparing-memory-allocation-methods.md)

 

 



