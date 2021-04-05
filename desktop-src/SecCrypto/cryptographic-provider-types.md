---
description: Das kryptografiefeld ist groß und wächst.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Typen von Kryptografieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e976909cec25b5194187d61d2e753eeb830c09f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750913"
---
# <a name="cryptographic-provider-types"></a>Typen von Kryptografieanbietern

Das [*kryptografiefeld*](../secgloss/c-gly.md) ist groß und wächst. Es gibt viele verschiedene Standarddaten Formate und-Protokolle. Diese sind im Allgemeinen in Gruppen oder Familien organisiert, von denen jeder über einen eigenen Satz von Datenformaten und Möglichkeiten zum Ausführen von Aufgaben verfügt. Auch wenn zwei Familien denselben Algorithmus verwenden (z. b. die [*RC2*](../secgloss/r-gly.md) - [*Blockchiffre*](../secgloss/b-gly.md)), werden häufig unterschiedliche [*Auffüll Schemas, unterschiedliche*](../secgloss/p-gly.md) [*Schlüssellängen*](../secgloss/k-gly.md)und verschiedene Standard Modi verwendet. CryptoAPI ist so konzipiert, dass ein CSP-Anbietertyp eine bestimmte Familie darstellt.

Wenn eine Anwendung eine Verbindung mit einem CSP eines bestimmten Typs herstellt, wird jede der kryptoapi-Funktionen standardmäßig in einer von der-Familie vorgeschriebenen Weise ausgeführt, die diesem CSP-Typ entspricht. Die Auswahl des Anbieter Typs einer Anwendung gibt die folgenden Elemente an:



| Element                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algorithmus für den Schlüsselaustausch*](../secgloss/k-gly.md)                | Jeder Anbietertyp gibt einen und nur einen Schlüsselaustausch Algorithmus an. Jeder CSP eines bestimmten Typs muss diesen Algorithmus implementieren. Anwendungen geben den zu verwendenden Schlüsselaustausch Algorithmus an, indem Sie einen CSP des entsprechenden Anbieter Typs auswählen.                                                        |
| [*Algorithmus für digitale Signaturen*](../secgloss/d-gly.md) | Jeder Anbietertyp gibt genau einen Algorithmus für die digitale Signatur an. Jeder CSP eines bestimmten Typs muss diesen Algorithmus implementieren. Anwendungen geben den zu verwendenden Algorithmus für die digitale Signatur an, indem Sie einen CSP des entsprechenden Anbieter Typs auswählen.                                              |
| Schlüssel-BLOB-Formate                                                                                                                    | Der Typ angeben bestimmt das Format des [*Schlüssel-BLOBs*](../secgloss/k-gly.md) , das zum Exportieren von Schlüsseln aus dem [*CSP*](../secgloss/c-gly.md) und zum Importieren von Schlüsseln in einen CSP verwendet wird. |
| Format der digitalen Signatur                                                                                                            | Der Anbietertyp bestimmt das Format der digitalen Signatur. Dadurch wird sichergestellt, dass eine Signatur, die von einem CSP eines bestimmten Anbieter Typs erstellt wird, von einem beliebigen CSP des gleichen Anbieter Typs überprüft werden kann.                                                                                                              |
| Sitzungsschlüssel-abderivationschema                                                                                                       | Der Anbietertyp bestimmt die Methode, die zum Ableiten eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Hash*](../secgloss/h-gly.md)verwendet wird.                                                                                   |
| [*Schlüssellänge*](../secgloss/k-gly.md)                                                    | Einige Anbieter Typen geben die Länge der [*öffentlichen/privaten Schlüsselpaare*](../secgloss/p-gly.md) und der Sitzungsschlüssel an.                                                                                                               |
| Standard Modi                                                                                                                       | Der Anbietertyp gibt häufig Standard Modi für verschiedene Optionen an, z. b. den Verschlüsselungs [*Modus*](../secgloss/c-gly.md) für die Block Verschlüsselung oder die [*Auffüllung*](../secgloss/p-gly.md) -Methode der Block Verschlüsselung.          |



 

Einige erweiterte Anwendungen können gleichzeitig eine Verbindung mit mehr als einem CSP herstellen, aber die meisten Anwendungen verwenden im Allgemeinen nur einen einzigen CSP.

Zurzeit gibt es eine Reihe von vordefinierten Anbieter Typen. In den nächsten Abschnitten finden Sie Informationen zu den folgenden Anbieter Typen:

-   [Prov \_ RSA \_ Full](prov-rsa-full.md)
-   [Prov \_ RSA \_ AES](prov-rsa-aes.md)
-   [Prov \_ RSA \_ sig](prov-rsa-sig.md)
-   [Prov \_ RSA \_ SChannel](prov-rsa-schannel.md)
-   [Prov- \_ DSS](prov-dss.md)
-   [Prov \_ DSS \_ dh](prov-dss-dh.md)
-   [Prov \_ dh \_ SChannel](prov-dh-schannel.md)
-   [Prov- \_ Fortezza](prov-fortezza.md)
-   [Prov \_ MS \_ Exchange](prov-ms-exchange.md)
-   [Prov- \_ SSL](prov-ssl.md)

Obwohl einige CSP-Typen möglicherweise teilweise mit anderen kompatibel sind, sollten zwei oder mehr Anwendungen, die Schlüssel und verschlüsselte Nachrichten [*austauschen*](../secgloss/e-gly.md) müssen, CSPs desselben Typs verwenden.

Ein benutzerdefinierter CSP-Writer kann einen neuen Anbietertyp definieren. Der CSP-Writer ist dann dafür verantwortlich, den neuen Anbietertyp an die Autoren aller Anwendungen zu verteilen, die ihn verwenden. Weitere Informationen zum Schreiben von benutzerdefinierten CSPs finden Sie unter [Kryptografiedienstanbieter](cryptographic-service-providers.md).

 

 
