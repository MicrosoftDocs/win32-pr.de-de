---
title: Unterstützung für IPX-Adress Zeichenfolgen in WinSNMP
description: WinSNMP 2,0 formalisiert die Verwendung von IPX-Adress Zeichenfolgen.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707313"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Unterstützung für IPX-Adress Zeichenfolgen in WinSNMP

WinSNMP 2,0 formalisiert die Verwendung von IPX-Adress Zeichenfolgen. Wenn Sie eine IPX-Adress Zeichenfolge als Eingabeparameter für die [**snmpstrautoentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) -Funktion angeben, müssen Sie die Zeichenfolge mit den folgenden Standards formatieren:

-   Eine Netzwerk Nummer, die aus acht hexadezimalen Ziffern besteht (bei Bedarf mit NULL gefüllt)
-   Ein Trennzeichen (":", "." oder "–")
-   Eine Knotennummer, die aus 12 hexadezimalen Ziffern besteht (bei Bedarf mit NULL gefüllt)

Beispiel: 00000001:00081a0d01c2 oder 00000001.00081 a0d01c2. Hexadezimale Ziffern können groß-oder Kleinbuchstaben sein.

Dies ist das Format, das die [**snmpentitytostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) -Funktion verwendet, um eine IPX-Adress Zeichenfolge zurückzugeben. Die Zeichenfolge wird zurückgegeben, wenn eine Anwendung, die in einem der nicht übersetzten Snmpapi-Modi betrieben wird, \_ die **snmpentitydestr** -Funktion aufruft. Die Zeichenfolge kann auch zurückgegeben werden, wenn die Anwendung im Snmpapi \_ -übersetzten Modus betrieben wird und kein benutzerfreundlicher Name für die Entität verfügbar ist.

 

 




