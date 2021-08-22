---
description: Das Microsoft-Telefonieprogrammiermodell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung, wodurch Endbenutzeranwendungen und Gerätehersteller von der Notwendigkeit abweicht, in Lockstep zu schreitet.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Microsoft-Telefonieprogrammiermodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33407069c8ff489006c3cb85e03b676126eca1abedf484d9d1bb5b1305677a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518644"
---
# <a name="microsoft-telephony-programming-model"></a>Microsoft-Telefonieprogrammiermodell

Das Microsoft-Telefonieprogrammiermodell abstrahiert die Kommunikationssteuerung von der Gerätesteuerung, wodurch Endbenutzeranwendungen und Gerätehersteller von der Notwendigkeit abweicht, in Lockstep zu schreitet. Bei Verwendung dieses Modells benötigt eine Endbenutzer- oder Serveranwendung keine ausführlichen Informationen zur Gerätesteuerung, und das Gerät muss nicht auf die Anwendung zugeschnitten werden. Anwendungen und Geräte können Innovationen durchlaufen und sich ändern, ohne sich gegenseitig für Kunden unbrauchbar zu machen.

Das folgende Diagramm veranschaulicht, wie diese Abstraktion erreicht wird.

![wie tapi die Kommunikationssteuerung von der Gerätesteuerung abstrahiert](images/tapicomp.png)

Diese Komponenten können als Repositorys mit speziellem Wissen betrachtet werden. Die TAPI-Anwendung (Telefonieanwendungsprogrammierungsschnittstelle) kennt die Benutzeranforderungen, die TAPI-DLL und TAPISRV verstehen die allgemeine Telefonie, und die Dienstanbieter (TSP und MSP) kennen die detaillierte Gerätesteuerung. Anwendungsautoren und Gerätehersteller benötigen nur allgemeine Kenntnisse der Anforderungen des jeweils anderen.

-   Eine Anwendung lädt die TAPI-DLL in ihren Prozessbereich und verwendet TAPI, um Anforderungen zu kommunizieren.
-   TAPI richtet eine RPC-Linkkommunikation mit dem TAPI-Server ein.
-   Darüber hinaus erstellt TAPI 3.x ein MSP-Objekt und kommuniziert mithilfe eines definierten Befehlssatzes, der Media Service Provider Interface (MSPI).
-   Wenn eine Anwendung einen TAPI-Vorgang aufruft, überprüft und marshallt die TAPI-Dynamic Link-Bibliothek die Parameter und leitet die Informationen dann an TAPISRV weiter.
-   TAPISRV verfolgt Kommunikationsressourcen, die für den lokalen Computer verfügbar sind, und Schnittstellen mit den Telefoniedienstanbietern (Telefoniedienstanbieter, TSPs) mithilfe der Telefoniedienstanbieterschnittstelle (Telefoniedienstanbieterschnittstelle, TSPI).
-   Die Kommunikation zwischen einem TSP und einem MSP erfolgt über eine virtuelle Verbindung, die die TAPI-DLL und TAPISRV durchläuft.
-   Das TSP-/MSP-Paar stellt Informationen zum Gerätezustand und zu den Funktionen zur Verfügung und implementiert die spezifischen Befehle, die für eine gewünschte Antwort erforderlich sind.

Das Ergebnis der Verwendung dieses Programmiermodells ist, dass Anwendungen Geräteänderungen ignorieren oder anpassen können und neue Geräte sofort nützlich sein können, anstatt auf Codebasisänderungen zu warten. Der potenzielle Marktanteil wird sowohl für Anwendungsautoren als auch für Gerätehersteller erweitert.

In den folgenden Themen werden die Microsoft-Telefoniekomponenten ausführlicher beschrieben:

-   [TAPI-Anwendungen](tapi-applications.md)
-   [TAPI-DLL](tapi-dll.md)
-   [TAPI-Server](tapi-server.md)
-   [Dienstleister](service-providers.md)
-   [Synchrones/asynchrones Modell](synchronous-asynchronous-model.md)
-   [TAPI-Datenstrukturen](tapi-data-structures.md)
-   [TAPI-Dienstebenen](tapi-levels-of-service.md)

 

 



