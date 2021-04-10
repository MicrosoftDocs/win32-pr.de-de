---
description: Transport Adressen (xaddrs), die in Probe Matches-und resolvematches-Meldungen enthalten sind, unterliegen der grundlegenden Validierung, bevor WSDAPI eine HTTP-Nachricht sendet, z. b. eine metadatenanforderung.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Xaddr-Validierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215303"
---
# <a name="xaddr-validation-rules"></a>Xaddr-Validierungsregeln

Transport Adressen (xaddrs), die in [Probe Matches](probematches-message.md) -und [resolvematches](resolvematches-message.md) -Meldungen enthalten sind, unterliegen der grundlegenden Validierung, bevor WSDAPI eine HTTP-Nachricht sendet, z. b. eine metadatenanforderung.

Dadurch wird sichergestellt, dass sich die xaddrs im gleichen Subnetz wie der Client befinden.

Der folgende XML-Code zeigt ein xaddrs-Beispiel Element. Das WSD-Präfix verweist auf den-Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Alle folgenden Bedingungen müssen erfüllt sein, damit die HTTP-Nachricht über das Netzwerk gesendet wird.

-   Xaddrs muss eine HTTP-oder HTTPS-Adresse sein. Xaddrs anderer Schemas werden ignoriert.
-   Wenn HTTPS-xaddrs vorhanden sind, müssen alle xaddrs HTTPS lauten. Xaddr-Abschnitte, die sowohl HTTP-als auch HTTPS-Adressen enthalten, werden vollständig ignoriert. Außerdem muss die Endpunkt Adresse des Geräts exakt mit den HTTPS-xaddrs übereinstimmen.
-   Xaddrs müssen IP-Adressen oder Hostnamen sein, die über DNS aufgelöst werden können. Normalerweise werden IP-Adressen verwendet.
-   Mindestens eine IP-Adresse, die in den xaddrs enthalten ist (oder die IP-Adresse, die von einem in den xaddrs enthaltenen Hostnamen aufgelöst wurde), muss sich im gleichen Subnetz befinden wie der Adapter, über den die [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Nachricht empfangen wurde.
-   Auf die Adresse und den Port, die in der ersten xaddr angegeben sind, muss zugegriffen werden können. WSDAPI versucht, eine Verbindung mit dieser Adresse herzustellen, wenn eine HTTP-Verbindung hergestellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Probe Matches](probematches-message.md)
</dt> <dt>

[Resolvematches](resolvematches-message.md)
</dt> <dt>

[Ermittlungs-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



