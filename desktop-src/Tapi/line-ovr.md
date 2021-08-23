---
description: Das Linienkonzept hat sich im Laufe der Zeit weiterentwickelt und wurde teilweise durch die Konzepte Adresse und Terminal ersetzt. TAPI 3 verwendet nicht direkt das Konzept der Linie, aber TAPI 2 integriert dieses Paradigma weiterhin.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c299924a69d3e6e4889d14a72a571ca11ed2dc9e97514702f8ba4836f4c5b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660204"
---
# <a name="line"></a>Linie

Das Linienkonzept hat sich im Laufe der Zeit weiterentwickelt und wurde teilweise durch die Konzepte Adresse und Terminal ersetzt. TAPI 3 verwendet nicht direkt das Konzept der Linie, aber TAPI 2 integriert dieses Paradigma weiterhin.

Ein *Liniengerät ist* ein physisches Gerät, z. B. ein Faxboard, ein Modem oder eine ISDN-Karte, die mit einem Netzwerk verbunden ist. Das Gerät ist möglicherweise nicht physisch mit dem Computer verbunden, auf dem die TAPI-Anwendung ausgeführt wird, z. B. mit einem Modempool auf einem Server. Liniengeräte unterstützen Kommunikationsfunktionen, indem anwendungen das Senden von Informationen an ein Netzwerk oder das Empfangen von Informationen aus einem Netzwerk ermöglichen. Ein Liniengerät enthält einen Satz von homogenen Kanälen, die zum Einrichten von Aufrufen verwendet werden können.

In TAPI 2.x-Anwendungen ist ein Liniengerät die logische Darstellung eines physischen Telefongeräts. Obwohl "line" häufig etwas mit zwei Endpunkten bezeichnet, ist es möglich, ein Liniengerät an einen einzelnen Punkt zu abstrahieren, da TAPI es nur als Einstiegspunkt in die Zeile betrachtet, die zum Switch führt.

![Liniengeräte](images/ch0501.png)

Obwohl die drei Zeilen in der obigen Abbildung aus unterschiedlicher Hardware bestehen und für verschiedene Funktionen verwendet werden, werden sie nach demselben Gerätetyp abstrahiert und durch dieselben Regeln bestimmt. Das Telefon stellt kein Telefongerät dar, sondern ein Telefon, das für Sprachanrufe verwendet wird. Wenn sie dieses Liniengerät für eingehende oder ausgehende Anrufe verwendet, muss die Anwendung auch eine Instanz der Phone-Device-Klasse öffnen und steuern, die in späteren Abschnitten ausführlich beschrieben wird.

Die Line Device-Klasse ist eine geräteunabhängige Darstellung eines physischen Liniengeräts, z. B. eines Modems. Sie kann einen oder mehrere identische Kommunikationskanäle (für Signalisierung und/oder Informationen) zwischen der Anwendung und dem Switch oder Netzwerk enthalten. Da Kanäle, die zu einer einzelnen Zeile gehören, identische Funktionen haben, sind sie austauschbar. In vielen Fällen modelliert ein Dienstanbieter (wie beiFALLS) eine Linie so, dass sie nur einen Kanal hat. Andere Technologien wie ISDN bieten mehr Kanäle, und der Dienstanbieter sollte sie entsprechend behandeln.

**TAPI 2.x:** Anwendungen entdecken Linienfunktionen mithilfe [**der lineGetDevCaps-Funktion.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) Die Versionsaushandlung [**mithilfe der lineNegotiateAPIVersion-LineNegotiateExtVersion-Funktionen**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) muss zuvor aufgerufen worden sein.

**TAPI 3.x:** Anwendungen basieren in erster Linie auf dem Adresskonzept.

 

 
