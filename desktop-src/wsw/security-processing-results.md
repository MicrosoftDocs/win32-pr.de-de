---
title: Ergebnisse der Sicherheits Verarbeitung
description: Auf einem sicheren Kanal werden nur die Nachrichten, die erfolgreich Sicherheitsüberprüfungen bestanden haben, an die Anwendung übermittelt.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Sicherheitsverarbeitungs Ergebnisse Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106340948"
---
# <a name="security-processing-results"></a>Ergebnisse der Sicherheits Verarbeitung

Auf einem sicheren Kanal werden nur die Nachrichten, die erfolgreich Sicherheitsüberprüfungen bestanden haben, an die Anwendung übermittelt. Für diese Nachrichten werden einige Ergebnisse aus der Sicherheitsüberprüfung als Nachrichten Eigenschaften angefügt, und die Anwendung kann diese Eigenschaften extrahieren und untersuchen, um zusätzliche Schritte auszuführen, z. b. Autorisierungs Überprüfungen.


Die Funktion [**wsgetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) kann verwendet werden, um alle sicherheitsbezogenen Eigenschaften abzurufen, die in der [**WS- \_ Nachrichten eigen schafts- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)definiert sind. **Wsgetmessageproperty** gibt einen Fehler für Abfragen zurück, die Sicherheitseigenschaften anfordern, die nicht für den auf dem Kanal verwendeten Sicherheitstyp gelten. Die Nachricht ist weiterhin Besitzer der von der Abfragefunktion zurückgegebenen Eigenschaften.

Die folgenden API-Elemente werden mit den Ergebnissen der Sicherheits Verarbeitung verwendet.

| Enumeration                                                                | Beschreibung                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**WS- \_ Sicherheits \_ Token-Eigenschaften- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Definiert die Schlüssel für die Felder und Eigenschaften, die aus einem Sicherheits Token extrahiert werden können. |



 



| Funktion                                                         | BESCHREIBUNG                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**Wsgetsecuritytoken-Eigenschaft**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrahiert ein Feld oder eine Eigenschaft aus einem Sicherheits Token. |



 



| Handle                                       | BESCHREIBUNG                                     |
|----------------------------------------------|-------------------------------------------------|
| [WS- \_ Sicherheits \_ Token](ws-security-token.md) | Ein undurchsichtiges handle, das ein Sicherheits Token darstellt. |



 

 

 




