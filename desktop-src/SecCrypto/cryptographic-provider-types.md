---
description: Das Feld der Kryptografie ist groß und wächst.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Kryptografieanbietertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaeee585ff9c11e2a20a201f541f3cd147aef6e9b50c37d60156e75a1b9fd94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876210"
---
# <a name="cryptographic-provider-types"></a>Kryptografieanbietertypen

Das Feld der [*Kryptografie*](../secgloss/c-gly.md) ist groß und wächst. Es gibt viele verschiedene Standarddatenformate und -protokolle. Diese sind im Allgemeinen in Gruppen oder Familien organisiert, von denen jede über einen eigenen Satz von Datenformaten und eine eigene Vorgehensweise verfügt. Auch wenn zwei Familien denselben Algorithmus verwenden (z. B. die [*RC2-Blockchiffre),*](../secgloss/b-gly.md)verwenden sie häufig unterschiedliche [*Auffüllschemas,*](../secgloss/p-gly.md) unterschiedliche [*Schlüssellängen*](../secgloss/k-gly.md)und unterschiedliche Standardmodi. [](../secgloss/r-gly.md) CryptoAPI ist so konzipiert, dass ein CSP-Anbietertyp eine bestimmte Familie darstellt.

Wenn eine Anwendung eine Verbindung mit einem CSP eines bestimmten Typs herstellt, funktioniert jede der CryptoAPI-Funktionen standardmäßig auf eine Weise, die von der Familie vorgegeben wird, die diesem CSP-Typ entspricht. Die Auswahl des Anbietertyps einer Anwendung gibt die folgenden Elemente an:



| Element                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Schlüsselaustauschalgorithmus*](../secgloss/k-gly.md)                | Jeder Anbietertyp gibt einen und nur einen Schlüsselaustauschalgorithmus an. Jeder CSP eines bestimmten Typs muss diesen Algorithmus implementieren. Anwendungen geben den zu verwendenden Schlüsselaustauschalgorithmus an, indem sie einen CSP des entsprechenden Anbietertyps auswählen.                                                        |
| [*Algorithmus für digitale Signaturen*](../secgloss/d-gly.md) | Jeder Anbietertyp gibt einen und nur einen digitalen Signaturalgorithmus an. Jeder CSP eines bestimmten Typs muss diesen Algorithmus implementieren. Anwendungen geben den zu verwendenden Digitalen Signaturalgorithmus an, indem sie einen CSP des entsprechenden Anbietertyps auswählen.                                              |
| Schlüsselblobformate                                                                                                                    | Der Bereitstellungstyp bestimmt das Format des [*Schlüssel-BLOB,*](../secgloss/k-gly.md) das zum Exportieren von Schlüsseln aus dem [*CSP*](../secgloss/c-gly.md) und zum Importieren von Schlüsseln in einen CSP verwendet wird. |
| Digitales Signaturformat                                                                                                            | Der Anbietertyp bestimmt das digitale Signaturformat. Dadurch wird sichergestellt, dass eine Signatur, die von einem CSP eines bestimmten Anbietertyps erstellt wird, von jedem CSP desselben Anbietertyps überprüft werden kann.                                                                                                              |
| Ableitungsschema für Sitzungsschlüssel                                                                                                       | Der Anbietertyp bestimmt die Methode, mit der ein [*Sitzungsschlüssel*](../secgloss/s-gly.md) von einem [*Hash*](../secgloss/h-gly.md)abgeleitet wird.                                                                                   |
| [*Schlüssellänge*](../secgloss/k-gly.md)                                                    | Einige Anbietertypen geben die Länge von Paaren aus öffentlichen und [*privaten Schlüsseln*](../secgloss/p-gly.md) und sitzungsschlüsseln an.                                                                                                               |
| Standardmodi                                                                                                                       | Der Anbietertyp gibt häufig Standardmodi für verschiedene Optionen an, z. B. den [*Verschlüsselungsmodus*](../secgloss/c-gly.md) für blockverschlüsselung oder die [*Blockverschlüsselungsauffüllungsmethode.*](../secgloss/p-gly.md)          |



 

Einige erweiterte Anwendungen stellen möglicherweise eine Verbindung mit mehreren CSP gleichzeitig her, aber die meisten Anwendungen verwenden in der Regel nur einen einzigen CSP.

Derzeit gibt es eine Reihe vordefinierter Anbietertypen. Die nächsten Abschnitte enthalten Informationen zu den folgenden Anbietertypen:

-   [PROV \_ RSA \_ FULL](prov-rsa-full.md)
-   [PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROV \_ RSA \_ SCHANNEL](prov-rsa-schannel.md)
-   [PROV \_ DSS](prov-dss.md)
-   [PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ SCHANNEL](prov-dh-schannel.md)
-   [PROV \_ FORTEZZA](prov-fortezza.md)
-   [PROV \_ MS \_ EXCHANGE](prov-ms-exchange.md)
-   [PROV \_ SSL](prov-ssl.md)

Obwohl einige CSP-Typen teilweise mit anderen kompatibel sein können, sollten zwei oder mehr Anwendungen, die Schlüssel und verschlüsselte Nachrichten [*austauschen*](../secgloss/e-gly.md) müssen, CSPs desselben Typs verwenden.

Ein benutzerdefinierter CSP-Writer kann einen neuen Anbietertyp definieren. Der CSP Writer ist dann jedoch für die Verteilung des neuen Anbietertyps an die Autoren aller Anwendungen verantwortlich, die ihn verwenden sollen. Informationen zum Schreiben von benutzerdefinierten CSPs finden Sie unter [Kryptografiedienstanbieter.](cryptographic-service-providers.md)

 

 
