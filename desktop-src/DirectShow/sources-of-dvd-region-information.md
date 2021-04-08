---
description: Quellen der DVD-Regions Informationen
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Quellen der DVD-Regions Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960169"
---
# <a name="sources-of-dvd-region-information"></a>Quellen der DVD-Regions Informationen

Es gibt drei Quellen für DVD-Regions Informationen, die zusammenarbeiten, um die Region für die DVD-Wiedergabe auf einem Windows-PC zu ermitteln.

-   DVD-Titel. Die meisten DVD-Titel werden für eine bestimmte Region markiert. Einige Titel können nur in einer Region abgespielt werden, einige können in mehreren Regionen abgespielt werden, und andere können alle Bereiche wiedergegeben werden. Die Bereiche 1 bis 6 wurden in der ursprünglichen DVD-Video Spezifikation definiert. Region 7 ist zurzeit nicht definiert. Region 8 wurde in 1999 für besondere Orte, z. b. für Flugzeuge, hinzugefügt. DVD-ROM-Laufwerke (solche ohne Videothek) dürfen keine Regions Codierung enthalten.
-   DVD-ROM-Laufwerk. Es gibt zwei Arten von DVD-ROM-Laufwerken: RPC1-Laufwerke (RPC-Phase 1) und rpc2-Laufwerke (RPC Phase 2). RPC1-Laufwerke verfügen über keine integrierte Hardwareunterstützung für die Regions Verwaltung. Bei diesen Laufwerken behält Windows die Informationen zur Anzahl der Regions Änderungen bei, und die Region kann nur ein Mal geändert werden. Rpc2-Laufwerke behalten die Anzahl der Regions Änderungs Informationen auf der Hardware bei, und im Allgemeinen kann die Region solcher Laufwerke bis zu fünfmal geändert werden.
-   DVD-Decoder. Einige DVD-Decoders, Hardware oder Software werden für eine bestimmte Region festgelegt. Im Allgemeinen kann der Benutzer den Bereich des Decoders nicht ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung der Änderung von DVD-Regionen in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



