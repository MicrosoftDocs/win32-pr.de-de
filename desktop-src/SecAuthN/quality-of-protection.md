---
description: Die durch die qop-Direktive identifizierte Schutzqualität wird zuerst vom Server in der Digest-Abfrage angegeben und dann vom Client in der Abfrageantwort bestätigt.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualität des Schutzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202acbf319601af74efc35117990f27cc6edff76f27da243453f82bf50984977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920449"
---
# <a name="quality-of-protection"></a>Qualität des Schutzes

Die durch die qop-Direktive identifizierte Schutzqualität wird zuerst vom Server in der Digest-Abfrage angegeben und dann vom Client in der Abfrageantwort bestätigt. Wenn der Client eine Schutzqualität erfordert, die der Server nicht unterstützt, muss der Client die Authentifizierung beenden.

Die möglichen Werte für die qop-Direktive werden in der folgenden Tabelle beschrieben.



| Wert                   | BESCHREIBUNG                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| "Authentifizierung"                  | Nur Authentifizierung.                                                                                                                         |
| "auth-int"              | Authentifizierungs- und [*Integritätsüberprüfung*](../secgloss/i-gly.md) mithilfe von Signaturen.                  |
| (nur SASL) "auth-conf" | Authentifizierung, Integritäts- und Vertraulichkeitsprüfung mithilfe von Signaturen und Verschlüsselung. Weitere Informationen finden Sie unter [Verschlüsselungen.](ciphers.md) |



 

Die Qualität des Schutzes wird durch Kontextanforderungsflags bestimmt, die an den Microsoft Digest SSP übergeben werden. In der folgenden Tabelle sind die Flags im Zusammenhang mit der Qualität des Schutzes und der resultierende Wert der qop-Direktive aufgeführt.



| Flag                         | qop-Wert               |
|------------------------------|-------------------------|
| *XXX* \_ \_REQ-VERTRAULICHKEIT  | "auth-conf" (nur SASL) |
| *XXX* \_ REQ \_ REPLAY \_ DETECT   | "auth-int"              |
| *XXX* \_ REQ \_ SEQUENCE \_ DETECT | "auth-int"              |
| *XXX* \_ REQ \_ INTEGRITY        | "auth-int"              |
| (none)                       | "Authentifizierung"                  |



 

> [!Note]  
> Kontextanforderungsflags, die von Serveranwendungen angegeben werden, haben das Präfix ASC, und den von Clients angegebenen Flags wird isc das Präfix vorangestellt. Um die von Ihrer Anwendung verwendeten Flagwerte zu bestimmen, ersetzen Sie *XXX* durch eines dieser Präfixe.

 

Weitere serverbezogene Informationen finden Sie unter [Generieren der Digest-Herausforderung.](generating-the-digest-challenge.md)

Weitere clientbezogene Informationen finden Sie unter [Generieren der Digest-Abfrageantwort.](generating-the-digest-challenge-response.md)

 

 
