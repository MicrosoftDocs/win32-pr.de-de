---
description: Die Security Service Provider Interface (SSPI) bietet eine universelle, branchenübliche Oberfläche für sichere verteilte Anwendungen.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Sicherheits Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347516"
---
# <a name="security-service-providers"></a>Sicherheits Dienstanbieter

Die Security Service Provider Interface (SSPI) bietet eine universelle, branchenübliche Oberfläche für sichere verteilte Anwendungen. Die Peer-grapherstellungs-API bietet Anwendungen die Möglichkeit, Links in einem Diagramm zu schützen, indem ein Sicherheits Dienstanbieter (SSP) angegeben wird. Hierbei handelt es sich um eine DLL, die eine SSPI-Schnittstelle implementiert. Eine Anwendung gibt einen SSP an, wenn ein Graph mithilfe von " [**Peer Graph Create**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)" erstellt wird.

Weitere Informationen zum Erstellen eines eigenen SSP finden Sie in der SSPI-Dokumentations Verknüpfung in der Liste der [Diagramm Verweis Links](graphing-reference-links.md).

## <a name="programming-considerations-for-implementing-an-ssp"></a>Programmier Überlegungen für die Implementierung eines SSP

Gehen Sie beim Aufrufen einer Anwendung innerhalb eines SSP mit Bedacht vor. Die folgenden Überlegungen gelten für SSP-Rückrufe:

-   Rückrufe sollten nicht lange dauern, da Sie während der Verbindungs Aushandlung aufgerufen werden. Wenn es zu lange dauert, bis eine Verbindung hergestellt ist, kann die Verbindung gelöscht werden.
-   Die Peer-grapherstellungs-API passt die Verbindungs Timeout Werte basierend auf der tatsächlichen Auslastung eines Systems dynamisch an. Der niedrigste Timeout Wert beträgt 20 Sekunden.
-   Um potenzielle Deadlocksituationen zu vermeiden, darf eine Anwendung nicht über einen Rückruf auf die Peer-graphingdatenbank zugreifen. Wenn eine Anwendung Informationen aus der graphingdatenbank benötigt, kann die Anwendung die erforderlichen Informationen zwischenspeichern und dann innerhalb des Rückrufs auf den Cache verweisen. Das Caching kann auch helfen, die Verbindungszeit zu verkürzen.

Beim Aufrufen der SSPI-Einstiegspunkte benötigt die Peer graphinginfrastruktur bestimmte Werte für bestimmte Parameter von fünf (5) Funktionen. Diese Parameterwerte können nicht in SSP geändert werden, und der SSP kann entweder die Werte für die fünf Parameter ignorieren oder Sie ordnungsgemäß behandeln. In der folgenden Liste sind diese spezifischen Parameter und die erforderlichen Werte aufgeführt:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Geben Sie einen (1) für den *pvgetkeyargument* -Parameter an. Gibt **null** für die Parameter *pszprincipal*, *pvlogonid* und *pgetkeyfn* an.

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Geben Sie die folgenden Flags für den Parameter " *f* " für den Parameter "f" an: **ISC \_ req \_ Mutual \_ auth ISC req Vertraulichkeit ISC req-Integrität ISC req Sequence erkennen von ISC req \| \_ \_ \| \_ \_ \| \_ \_ \_ \| \_ \_ Stream \| ISC \_ req \_ \_ Speicher zuweisen**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Geben Sie die folgenden Flags für den Parameter " *f-treq* " an: **ASC \_ req \_ Mutual \_ auth \| ASC \_ req \_ Vertraulichkeit \| ASC \_ req Integrity ASC req Sequence Detect ASC req \_ \| \_ \_ \_ \| \_ \_ Stream \| ASC \_ req \_ \_ Speicher zuweisen**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Geben Sie NULL (0) für *die Parameter* "vollständig" und " *messageseqno* " an.

-   [**DecryptMessage**](graphing-reference-links.md)

    Geben Sie 0 (null) für den *messageseqno* -Parameter und **null** für den *pfqop* -Parameter an.

Beim Aufrufen von " [**verschlüsseltmessage**](graphing-reference-links.md)" werden vier Puffer in der **secbufferdesc** -Struktur übermittelt. In der folgenden Tabelle wird die Reihenfolge angegeben, in der die Puffer übergeben werden

| SSP-spezifische Struktur         | BESCHREIBUNG                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **secbuffer \_ - \_ Streamheader**  | Enthält die Sicherheits Header Daten. Die Größe des Header Puffers wird durch Aufrufen von [**QueryContextAttributes**](graphing-reference-links.md) und angeben des Attributs " **secpkg \_ attr \_ Stream \_ sizes** " abgerufen.  |
| **secbuffer- \_ Daten**            | Enthält die zu verschlüsselnde klar Textnachricht.                                                                                                                                                                  |
| **secbuffer- \_ streamnachspann \_** | Enthält die Sicherheits Nachspann Daten. Die Größe des Header Puffers wird durch Aufrufen von [**QueryContextAttributes**](graphing-reference-links.md) und angeben des Attributs " **secpkg \_ attr \_ Stream \_ sizes** " abgerufen. |
| **secbuffer ist \_ leer.**           | Nicht initialisiert. Die Größe dieses Puffers ist 0 (null).                                                                                                                                                             |



 

Wenn [**DecryptMessage**](graphing-reference-links.md)aufgerufen wird, übergibt die Peer-graphingapi genau vier **secbuffer** -Strukturen. Der erste Puffer ist " **secbuffer \_ Data**" und enthält eine verschlüsselte Nachricht. Die restlichen Puffer werden für die Ausgabe verwendet und sind vom Typ " **secbuffer \_ empty**".

Der SSP muss die Verschlüsselung und Entschlüsselung von Benutzerdaten Puffern mit einer Größe von 16K und höher in einem einzigen-Befehl unterstützen.

 

 



