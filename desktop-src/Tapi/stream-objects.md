---
description: Streamobjekte sind eine Abstraktion des Mediendaten Stroms oder von Streams, die einer-sitzungssitzung zugeordnet sind.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Streamobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363558"
---
# <a name="stream-objects"></a>Streamobjekte

Streamobjekte sind eine Abstraktion des Mediendaten Stroms oder von Streams, die einer-sitzungssitzung zugeordnet sind. Die Schnittstellen und Methoden, die auf Stream-und substreamobjekten verfügbar gemacht werden, ermöglichen einer Anwendung das Ausführen sehr ausführlicher Steuerelemente, wie z. b. das Anhalten eines Streams, das Hinzufügen neuer Medientypen zu einer Kommunikationssitzung oder das Anpassen des audiovolumens eines bestimmten Konferenzteilnehmer.

Die zwei Haupttypen von Stream sind der Stream und der substream. Die Schnittstellen und Methoden einer Standard Implementierung sind sowohl für als auch für substreaming ähnlich, das eine niedrigere Steuerungsebene zulässt. Alle Medien Dienstanbieter (MSPs) müssen die grundlegenden Stream-Steuerungs Schnittstellen implementieren, aber die Unterstützung für untergeordnete Datenströme ist optional.

Außerdem implementieren einige Dienstanbieter [anbieterspezifische Schnittstellen](provider-specific-interfaces.md) für Datenströme. Der ipconf-MSP stellt z. b. Steuerelemente auf Teilnehmerebene bereit. Eine Zusammenfassung finden Sie unter [ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md) . Weitere Schnittstellen, die implementiert werden können, finden Sie in der Dokumentation des Dienstanbieters.

MSP und TAPI erstellen Stream-Objekte für einen-Befehl während der anfänglichen Einrichtung einer ausgehenden oder eingehenden Sitzung. Die Anwendung ist dafür verantwortlich, die entsprechenden Terminals für diese Streams zu identifizieren und die Terminals auf den Streams auszuwählen.

Beachten Sie, dass in einigen Fällen ein MSP erfordert, dass die Anwendung Datenströme vor bestimmten Sitzungs Sitzungs Vorgängen beendet oder anhält.

Die Stream-Schnittstellen sind in der [MSPi-Referenz (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md)dokumentiert.

Das Beispiel zum [Auswählen eines Terminal](select-a-terminal.md) Codes zeigt ein Beispiel für das Auflisten von Streams und das Auswählen von Terminals auf diesen.

 

 



