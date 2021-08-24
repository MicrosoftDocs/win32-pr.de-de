---
description: Quellen von DVD-Regionsinformationen
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Quellen von DVD-Regionsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729dc02d07b927dd2bb7938ba87c6435df04459ad3ebd1976ede808bd292552e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904095"
---
# <a name="sources-of-dvd-region-information"></a>Quellen von DVD-Regionsinformationen

Es gibt drei Quellen von DVD-Regionsinformationen, die zusammenarbeiten, um den Bereich für die DVD-Wiedergabe auf einem Windows PC zu bestimmen.

-   DVD-Titel. Die meisten DVD-Titel sind für eine bestimmte Region gekennzeichnet. Einige Titel können nur in einer Region, einige in mehreren Regionen und andere in allen Regionen wiedergegeben werden. Die Regionen 1 bis 6 wurden in der ursprünglichen DVD-Video Spezifikation definiert. Region 7 ist derzeit nicht definiert. Region 8 wurde 1999 für spezielle Veranstaltungsorte wie Flugzeugen hinzugefügt. DVD-ROM-Datenträger (datenträger ohne Videozone) dürfen keine Regionscodierung enthalten.
-   DVD-ROM-Laufwerk. Es gibt zwei Arten von DVD-ROM-Laufwerken: RPC Phase 1-Laufwerke (RPC1) und RPC Phase 2-Laufwerke (RPC2). RPC1-Laufwerke verfügen nicht über integrierte Hardwareunterstützung für die Regionsverwaltung. Für diese Laufwerke verwaltet Windows die Informationen zur Änderungsanzahl der Region, und die Region kann nur einmal geändert werden. RPC2-Laufwerke verwalten die Informationen zur Regionsänderungsanzahl in der Hardware, und im Allgemeinen kann die Region dieser Laufwerke bis zu fünfmal geändert werden.
-   DVD-Decoder. Einige DVD-Decoder, Hardware oder Software, werden für eine bestimmte Region festgelegt. Im Allgemeinen kann der Benutzer die Region des Decoders nicht ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung für DVD-Regionsänderungen in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



