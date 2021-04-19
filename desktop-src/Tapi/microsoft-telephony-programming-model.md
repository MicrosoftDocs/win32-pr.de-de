---
description: Das Microsoft-telefonieprogrammierungs Modell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung und gibt Endbenutzer Anwendungen und Gerätehersteller von der Notwendigkeit, im Sperr Schritt zu wechseln, frei.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Microsoft Telefonie-Programmiermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343027"
---
# <a name="microsoft-telephony-programming-model"></a>Microsoft Telefonie-Programmiermodell

Das Microsoft-telefonieprogrammierungs Modell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung und gibt Endbenutzer Anwendungen und Gerätehersteller von der Notwendigkeit, im Sperr Schritt zu wechseln, frei. Die Verwendung dieses Modells erfordert keine detaillierten Informationen zur Gerätesteuerung, und das Gerät muss nicht auf die Anwendung zugeschnitten werden. Anwendungen und Geräte können Innovationen durchlaufen und sich ändern, ohne dass Sie für Kunden nutzlos werden.

Im folgenden Diagramm wird veranschaulicht, wie diese Abstraktion erreicht wird.

![Zusammenfassung der Kommunikationssteuerung durch TAPI von der Gerätesteuerung](images/tapicomp.png)

Diese Komponenten können als Repository spezieller Kenntnisse angesehen werden. Die TAPI-Anwendung (Application Programming Interface, Anwendungsprogrammierschnittstelle) kennt die Benutzer Anforderungen, die TAPI-dll und "tapisrv" die allgemeine Telefonie und die Dienstanbieter (TSP und MSP) eine ausführliche Gerätesteuerung. Anwendungs Schreiber und Gerätehersteller benötigen nur allgemeine Kenntnisse der jeweiligen Anforderungen.

-   Eine Anwendung lädt die TAPI-dll in ihren Prozessbereich und verwendet TAPI, um die Anforderungen zu kommunizieren.
-   TAPI stellt eine RPC-Link Kommunikation mit dem TAPI-Server her.
-   Außerdem erstellt TAPI 3. x ein MSP-Objekt und kommuniziert mit dem Objekt mithilfe eines definierten Satzes von Befehlen, der Media Service Provider Interface (MSPi).
-   Wenn eine Anwendung einen TAPI-Vorgang aufruft, überprüft und marshallt die TAPI-Dynamic-Link-Bibliothek die Parameter und leitet die Informationen an tapisrv weiter.
-   Tapisrv verfolgt Kommunikationsressourcen, die für den lokalen Computer verfügbar sind, und stellt mit den Telefoniedienstanbietern (Service Provider Interface, TSPI) eine Schnittstelle mit den Telefoniedienstanbietern
-   Die Kommunikation zwischen einem TSP und einem MSP erfolgt über eine virtuelle Verbindung, die die TAPI-dll und den tapisrv durchläuft.
-   Das TSP/MSP-paar stellt Informationen zum Gerätestatus und zu den Funktionen bereit und implementiert die spezifischen Befehle, die für eine gewünschte Antwort erforderlich sind.

Das Ergebnis der Verwendung dieses Programmiermodells ist, dass Anwendungen Geräteänderungen ignorieren oder anpassen können. neue Geräte können sofort nützlich sein, anstatt auf Änderungen an der Codebasis zu warten. Der potenzielle Marktanteil wird sowohl für Anwendungs Schreiber als auch für Gerätehersteller erweitert.

In den folgenden Themen werden die Microsoft-Telefoniekomponenten ausführlicher beschrieben:

-   [TAPI-Anwendungen](tapi-applications.md)
-   [TAPI-dll](tapi-dll.md)
-   [TAPI-Server](tapi-server.md)
-   [Dienstanbieter](service-providers.md)
-   [Synchrones/Asynchrones Modell](synchronous-asynchronous-model.md)
-   [TAPI-Datenstrukturen](tapi-data-structures.md)
-   [TAPI-Dienst Ebenen](tapi-levels-of-service.md)

 

 



