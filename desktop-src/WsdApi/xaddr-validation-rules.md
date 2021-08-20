---
description: Transportadressen (XAddrs), die in ProbeMatches- und ResolveMatches-Nachrichten enthalten sind, unterliegen einer grundlegenden Überprüfung, bevor WSDAPI eine HTTP-Nachricht sendet, z. B. eine Metadatenanforderung.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: XAddr-Validierungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3b167101b6012bcf20779381993cfff4ea7ea22d35eef5397ac1349baa2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049508"
---
# <a name="xaddr-validation-rules"></a>XAddr-Validierungsregeln

Transportadressen (XAddrs), die in [ProbeMatches-](probematches-message.md) und [ResolveMatches-Nachrichten](resolvematches-message.md) enthalten sind, unterliegen einer grundlegenden Überprüfung, bevor WSDAPI eine HTTP-Nachricht sendet, z. B. eine Metadatenanforderung.

Dadurch wird sichergestellt, dass sich die XAddrs im gleichen Subnetz wie der Client befinden.

Der folgende XML-Code zeigt ein XAddrs-Beispielelement. Das wsd-Präfix verweist auf den Namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Alle folgenden Bedingungen müssen erfüllt sein, bevor die HTTP-Nachricht über das Netzwerk gesendet wird.

-   XAddrs müssen HTTP- oder HTTPS-Adressen sein. XAddrs anderer Schemas werden ignoriert.
-   Wenn HTTPS-XAddrs vorhanden sind, müssen alle XAddrs HTTPS sein. XAddr-Abschnitte, die sowohl HTTP- als auch HTTPS-Adressen enthalten, werden vollständig ignoriert. Darüber hinaus muss die Endpunktadresse des Geräts genau mit den HTTPS-XAddrs übereinstimmen.
-   XAddrs müssen IP-Adressen oder Hostnamen sein, die über DNS auflösbar sind. In der Regel werden IP-Adressen verwendet.
-   Mindestens eine IP-Adresse, die in den XAddrs enthalten ist (oder ip address resolved from a hostname included in the XAddrs), muss sich im gleichen Subnetz befinden wie der Adapter, über den die [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) empfangen wurde.
-   Auf die Adresse und den Port, die im ersten XAddr angegeben sind, muss zugegriffen werden können. WSDAPI versucht, beim Herstellen einer HTTP-Verbindung eine Verbindung mit dieser Adresse herzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Ermittlung und Metadaten Exchange Nachrichtenmustern](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



