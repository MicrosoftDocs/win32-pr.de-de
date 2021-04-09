---
description: Die von der QoP-Direktive identifizierte Qualität des Schutzes wird zuerst vom Server in der digestfrage angegeben und dann vom Client in der Challenge-Antwort bestätigt.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualität des Schutzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050318"
---
# <a name="quality-of-protection"></a>Qualität des Schutzes

Die von der QoP-Direktive identifizierte Qualität des Schutzes wird zuerst vom Server in der digestfrage angegeben und dann vom Client in der Challenge-Antwort bestätigt. Wenn der Client eine Quality of Protection erfordert, die vom Server nicht unterstützt wird, muss der Client die Authentifizierung beenden.

Die möglichen Werte für die QoP-Direktive werden in der folgenden Tabelle beschrieben.



| Wert                   | BESCHREIBUNG                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Authentifizierung                  | Nur Authentifizierung.                                                                                                                         |
| "auth-int"              | Authentifizierungs-und [*Integritäts*](../secgloss/i-gly.md) Überprüfung mithilfe von Signaturen.                  |
| (Nur SASL) "auth-conf" | Authentifizierung, Integrität und Vertraulichkeits Überprüfung mithilfe von Signaturen und Verschlüsselung. Weitere Informationen finden Sie unter [Chiffren](ciphers.md). |



 

Die Qualität des Schutzes wird durch die an die Microsoft Digest SSP übergebenen anforderungsflags festgelegt. In der folgenden Tabelle werden die Flags im Zusammenhang mit der Qualität des Schutzes und der resultierende Wert der QoP-Direktive aufgelistet.



| Flag                         | QoP-Wert               |
|------------------------------|-------------------------|
| *Xxx* \_ req- \_ Vertraulichkeit  | "auth-conf" (nur SASL) |
| *Xxx* \_ req \_ Replay \_ Detect   | "auth-int"              |
| *Xxx* \_ req- \_ Sequenz \_ Erkennung | "auth-int"              |
| *Xxx* \_ req- \_ Integrität        | "auth-int"              |
| (none)                       | Authentifizierung                  |



 

> [!Note]  
> Von Server Anwendungen angegebene kontoanforderungsflags haben das Präfix ASC, und den Clients, die von Clients angegeben werden, wird das Präfix ISC bereitgestellt Um die von der Anwendung verwendeten Flagwerte zu ermitteln, ersetzen Sie eines dieser Präfixe für *xxx*.

 

Weitere Server bezogene Informationen finden Sie unter [Erstellen der Digest-Challenge](generating-the-digest-challenge.md).

Weitere Client bezogene Informationen finden Sie unter [Erstellen der Digest](generating-the-digest-challenge-response.md)-Abfrage Antwort.

 

 
