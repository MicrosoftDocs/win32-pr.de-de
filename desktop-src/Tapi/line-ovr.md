---
description: Das Linienkonzept wurde im Laufe der Zeit weiterentwickelt und wurde teilweise durch die Adress-und terminalkonzepte abgelöst. TAPI 3 verwendet nicht direkt das Konzept von Line, aber TAPI 2 verwendet dieses Paradigma weiterhin.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Zeile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8275555e0cb34f5831ce671e22a89a1499fb1796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556638"
---
# <a name="line"></a>Zeile

Das Linienkonzept wurde im Laufe der Zeit weiterentwickelt und wurde teilweise durch die Adress-und terminalkonzepte abgelöst. TAPI 3 verwendet nicht direkt das Konzept von Line, aber TAPI 2 verwendet dieses Paradigma weiterhin.

Ein *liniengerät* ist ein physisches Gerät, z. b. ein faxboard, ein Modem oder eine ISDN-Karte, die mit einem Netzwerk verbunden ist. Das Gerät ist möglicherweise nicht physisch mit dem Computer verbunden, auf dem die TAPI-Anwendung ausgeführt wird, z. b. ein Modem Pool auf einem Server. Line-Geräte unterstützen Kommunikationsfunktionen, indem Sie es Anwendungen ermöglichen, Informationen an ein Netzwerk zu senden oder von diesem zu empfangen. Ein liniengerät enthält einen oder mehrere homogene Kanäle, die zum Einrichten von Aufrufen verwendet werden können.

In TAPI 2. x-Anwendungen ist ein liniengerät die logische Darstellung eines physischen Telefons. Obwohl "Line" häufig etwas mit zwei Endpunkten anweist, ist es möglich, ein Linien Gerät an einen einzelnen Punkt zu abstrahieren, da TAPI es nur als Einstiegspunkt für die Linie anzeigt, die zum Switch führt.

![Linien Geräte](images/ch0501.png)

Obwohl die drei Zeilen in der obigen Abbildung aus unterschiedlichen Hardware zusammengesetzt und für verschiedene Funktionen verwendet werden, werden Sie auf denselben Gerätetyp abstrahiert und unterliegen denselben Regeln. Das Telefon stellt kein Telefongerät, sondern ein für Sprachanrufe verwendetes Zeilen Gerät dar. Wenn dieses Zeilen Gerät für eingehende oder ausgehende Aufrufe verwendet wird, muss die Anwendung auch eine Instanz der Telefongeräte Klasse öffnen und Steuern, die in späteren Abschnitten ausführlich beschrieben wird.

Bei der Line-Geräteklasse handelt es sich um eine geräteunabhängige Darstellung eines physischen Geräte Geräts, z. b. ein Modem. Es kann einen oder mehrere identische Kommunikationskanäle (zur Signalisierung und/oder Informationen) zwischen der Anwendung und dem Switch oder dem Netzwerk enthalten. Da Kanäle, die zu einer einzelnen Zeile gehören, über identische Funktionen verfügen, sind Sie austauschbar. In vielen Fällen (wie bei Pots) modelliert ein Dienstanbieter eine Zeile mit nur einem Kanal. Andere Technologien, wie z. b. ISDN, bieten mehr Kanäle, und der Dienstanbieter sollte Sie entsprechend behandeln.

**TAPI 2. x:** Anwendungen ermitteln Zeilen Funktionen mithilfe der [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) -Funktion. Die Versions Aushandlung mithilfe der [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**linenegotiateextversion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) -Funktionen muss bereits zuvor aufgerufen werden.

**TAPI 3. x:** Anwendungen basieren hauptsächlich auf dem Adress Konzept.

 

 
