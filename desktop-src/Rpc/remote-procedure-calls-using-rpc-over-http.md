---
title: Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy
description: In Webbrowserprogrammen wird häufig das Hypertext-Transportprotokoll (HTTP) als primäres Mittel zum Durchsuchen der World Wide Web verwendet.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Remoteprozeduraufruf RPC , Tasks, mit RPC/HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fedeb1700d798a616d3441b356f6f31867eed0399f412ed1f82923bcc4ac5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101660"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy

In Webbrowserprogrammen wird häufig das Hypertext-Transportprotokoll (HTTP) als primäres Mittel zum Durchsuchen der World Wide Web verwendet. HTTP wird daher derzeit auf den meisten Computern umfassend genutzt. Microsoft hat die Funktionen des Internetinformationsservers (IIS) erweitert, um Remoteprozeduraufrufdienste über HTTP bereitzustellen.

Mit der Rpc-over-HTTP-Implementierung von Microsoft (RPC über HTTP) können RPC-Clients eine sichere und effiziente Verbindung über das Internet mit RPC-Serverprogrammen herstellen und Remoteprozeduraufrufe ausführen. Dies erfolgt mithilfe eines Vermittlers, der als RPC-over-HTTP-Proxy oder einfach als RPC-Proxy bezeichnet wird.

Der RPC-Proxy wird auf einem IIS-Computer ausgeführt. Sie akzeptiert RPC-Anforderungen aus dem Internet, führt Authentifizierungs-, Validierungs- und Zugriffsüberprüfungen für diese Anforderungen durch. Wenn die Anforderung alle Tests besteht, leitet der RPC-Proxy die Anforderung an den RPC-Server weiter, der die eigentliche Verarbeitung ausführt. Mit RPC über HTTP kommunizieren RPC-Client und -Server nicht direkt. Stattdessen verwenden sie den RPC-Proxy als Vermittler. Dieses Modell wurde aus vielen Gründen ausgewählt. Weitere Informationen finden Sie unter [RPC über HTTP-Sicherheit.](rpc-over-http-security.md)

Dieser Abschnitt enthält eine Übersicht über RPC über HTTP in den folgenden Themen:

-   [Verwenden von HTTP als RPC-Transport](using-http-as-an-rpc-transport.md)
-   [RPC über HTTP-Sicherheit](rpc-over-http-security.md)
-   [Systemanforderungen und Interoperabilität für RPC über HTTP](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Konfigurieren von Computern für RPC über HTTP](configuring-computers-for-rpc-over-http.md)
-   [RPC über HTTP-Bereitstellungs-Empfehlungen](rpc-over-http-deployment-recommendations.md)

Informationen zu RPC über HTTP-Szenarien mit hohem Volumen finden Sie unter [Microsoft RPC Load Balancing](rpc-load-balancing.md).

 

 




