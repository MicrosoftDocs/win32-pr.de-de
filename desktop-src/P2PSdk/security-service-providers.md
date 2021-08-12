---
description: Die Security Service Provider Interface (SSPI) bietet eine universelle, branchenüblichen Schnittstelle für sichere verteilte Anwendungen.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Sicherheitsdienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b53353dc9ed3236ccca5d9a345053870151a7b79e004c5e2ea69e39944209b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612153"
---
# <a name="security-service-providers"></a>Sicherheitsdienstanbieter

Die Security Service Provider Interface (SSPI) bietet eine universelle, branchenüblichen Schnittstelle für sichere verteilte Anwendungen. Die Peer Graphing-API bietet Anwendungen die Möglichkeit, Links in einem Graphen zu sichern, indem ein Sicherheitsdienstanbieter (Security Service Provider, SSP) angegeben wird, bei dem es sich um eine DLL handelt, die eine SSPI-Schnittstelle implementiert. Eine Anwendung gibt einen SSP an, wenn sie mit [**PeerGraphCreate einen Graphen erstellt.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)

Weitere Informationen zum Erstellen eines eigenen SSP finden Sie unter dem Link zur SSPI-Dokumentation in der Liste [der Graphing Reference Links (Graphing-Referenzlinks).](graphing-reference-links.md)

## <a name="programming-considerations-for-implementing-an-ssp"></a>Überlegungen zur Programmierung bei der Implementierung eines SSP

Seien Sie vorsichtig, wenn Sie eine Anwendung aus einem SSP aufrufen. Die folgenden Überlegungen gelten für SSP-Rückrufe:

-   Die Rückgabe von Rückrufen sollte nicht lange dauern, da sie während der Verbindungsaushandlung aufgerufen werden. Wenn es zu lange dauert, bis eine Verbindung hergestellt wird, kann die Verbindung gelöscht werden.
-   Die Peer Graphing-API passt Verbindungs-Timeoutwerte basierend auf der tatsächlichen Auslastung eines Systems dynamisch an. Der niedrigste Timeoutwert beträgt 20 Sekunden.
-   Um potenzielle Deadlocksituationen zu vermeiden, darf eine Anwendung nicht über einen Rückruf auf die Peerdiagrammdatenbank zugreifen. Wenn eine Anwendung Informationen aus der Graphdatenbank benötigt, kann die Anwendung die erforderlichen Informationen zwischenspeichern und dann innerhalb des Rückrufs auf den Cache verweisen. Das Zwischenspeichern kann auch dazu beitragen, die Verbindungszeit zu verringern.

Beim Aufrufen der SSPI-Einstiegspunkte erfordert die Peer graphing-Infrastruktur bestimmte Werte für bestimmte Parameter von fünf (5) Funktionen. Sie können diese für SSP bereitgestellten Parameterwerte nicht ändern, und der SSP kann entweder die Werte für die fünf Parameter ignorieren oder ordnungsgemäß behandeln. In der folgenden Liste sind diese spezifischen Parameter und erforderlichen Werte aufgeführt:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Geben Sie eins (1) für den *parameter pvGetKeyArgument* an. Gibt **NULL für** die *Parameter pszPrincipal,* *pvLogonID* und *pGetKeyFn* an.

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Geben Sie die folgenden Flags für den *fContextReq-Parameter* an: **ISC \_ REQ \_ MUTUAL \_ AUTH \| ISC \_ REQ \_ CONFIDENTIALITY \| ISC \_ REQ \_ INTEGRITY \| ISC \_ REQ SEQUENCE DETECT \_ \_ \| ISC \_ REQ STREAM \_ \| ISC \_ REQ ALLOCATE \_ \_ MEMORY**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Geben Sie die folgenden Flags für den *Parameter fContextReq* an: **ASC \_ REQ \_ MUTUAL \_ AUTH \| ASC \_ REQ \_ CONFIDENTIALITY \| ASC \_ REQ INTEGRITY \_ \| ASC \_ REQ SEQUENCE DETECT \_ \_ \| ASC \_ REQ STREAM \_ \| ASC \_ REQ ALLOCATE \_ \_ MEMORY**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Geben Sie null (0) für *die Parameter fQOP* und *MessageSeqNo* an.

-   [**DecryptMessage**](graphing-reference-links.md)

    Geben Sie null (0) für den *MessageSeqNo-Parameter* und **NULL** für den *pfQOP-Parameter* an.

Beim Aufrufen [**von EncryptMessage**](graphing-reference-links.md)werden vier Puffer in der **SecBufferDesc-Struktur** übergeben. Die folgende Tabelle gibt die Reihenfolge an, in der die Puffer übergeben werden.

| SSP-spezifische Struktur         | Beschreibung                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_SECBUFFER-STREAMHEADER \_**  | Enthält die Sicherheitsheaderdaten. Die Größe des Headerpuffers wird durch Aufrufen von [**QueryContextAttributes**](graphing-reference-links.md) und Angeben des **SECPKG \_ ATTR \_ STREAM \_ SIZES-Attributs** abgerufen.  |
| **\_SECBUFFER-DATEN**            | Enthält die zu verschlüsselnde Nur-Text-Nachricht.                                                                                                                                                                  |
| **SECBUFFER \_ STREAM \_ TRAILER** | Enthält die Sicherheitstrailerdaten. Die Größe des Headerpuffers wird durch Aufrufen von [**QueryContextAttributes**](graphing-reference-links.md) und Angeben des **SECPKG \_ ATTR \_ STREAM \_ SIZES-Attributs** abgerufen. |
| **SECBUFFER \_ EMPTY**           | Nicht initialisiert. Die Größe dieses Puffers ist 0 (null).                                                                                                                                                             |



 

Beim Aufrufen [**von DecryptMessage**](graphing-reference-links.md)übergibt die Peer Graphing-API genau vier **SecBuffer-Strukturen.** Der erste Puffer ist **SECBUFFER \_ DATA** und enthält eine verschlüsselte Nachricht. Die verbleibenden Puffer werden für die Ausgabe verwendet und sind vom **Typ SECBUFFER \_ EMPTY**.

Der SSP muss das Verschlüsseln und Entschlüsseln von Benutzerdatenpuffern mit einer Größe von 16K und höher in einem Aufruf unterstützen.

 

 



