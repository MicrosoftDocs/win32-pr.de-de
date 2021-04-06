---
title: Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy
description: Internet Browser Programme verwenden normalerweise das Hypertext Transport-Protokoll (http) als primäres Mittel zum Durchsuchen der World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verwendung von RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947311"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a>Remoteprozeduraufrufe mit dem RPC-über-HTTP-Proxy

Internet Browser Programme verwenden normalerweise das Hypertext Transport-Protokoll (http) als primäres Mittel zum Durchsuchen der World Wide Web. HTTP sieht daher auf den meisten Computern heute eine umfassende Nutzung vor. Microsoft hat die Funktionen seines Internet Informations Servers (IIS) erweitert, um Remote Prozedur Aufrufe mithilfe von http bereitzustellen.

Mit der Microsoft RPC-over-HTTP-Implementierung (RPC über HTTP) können RPC-Clients eine sichere und effiziente Internet Verbindung mit RPC-Serverprogrammen herstellen und Remote Prozedur Aufrufe ausführen. Dies wird durch einen Vermittler, der als RPC-über-HTTP-Proxy bezeichnet wird, oder einfach durch den RPC-Proxy erreicht.

Der RPC-Proxy wird auf einem IIS-Computer ausgeführt. Er akzeptiert RPC-Anforderungen aus dem Internet, führt Authentifizierungs-, Validierungs-und Zugriffs Überprüfungen für diese Anforderungen aus. wenn die Anforderung alle Tests bestanden hat, leitet der RPC-Proxy die Anforderung an den RPC-Server weiter, der die tatsächliche Verarbeitung ausführt. Mit RPC über HTTP kommunizieren der RPC-Client und-Server nicht direkt. Stattdessen verwenden Sie den RPC-Proxy als Vermittler. Dieses Modell wurde aus vielen Gründen ausgewählt. Weitere Informationen finden Sie unter [RPC-über-HTTP-Sicherheit](rpc-over-http-security.md).

Dieser Abschnitt bietet eine Übersicht über RPC über http in den folgenden Themen:

-   [Verwenden von http als RPC-Transport](using-http-as-an-rpc-transport.md)
-   [RPC-über-HTTP-Sicherheit](rpc-over-http-security.md)
-   [System Anforderungen und Interoperabilität für RPC über http](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [Konfigurieren von Computern für RPC über http](configuring-computers-for-rpc-over-http.md)
-   [Empfehlungen für RPC-over-HTTP](rpc-over-http-deployment-recommendations.md)

Informationen zu großen RPC-über-HTTP-Szenarios finden Sie unter [Microsoft RPC-Lastenausgleich](rpc-load-balancing.md).

 

 




