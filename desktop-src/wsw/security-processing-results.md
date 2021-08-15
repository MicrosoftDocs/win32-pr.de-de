---
title: Ergebnisse der Sicherheitsverarbeitung
description: Auf einem sicheren Kanal werden nur nachrichten, die erfolgreich Sicherheitsüberprüfungen bestehen, an die Anwendung übermittelt.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Security Processing Results Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53009729b3d7f1c8ff6b9e38a054d8dbadf202b7a0caa4a92c7861232c8390a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962929"
---
# <a name="security-processing-results"></a>Ergebnisse der Sicherheitsverarbeitung

Auf einem sicheren Kanal werden nur nachrichten, die erfolgreich Sicherheitsüberprüfungen bestehen, an die Anwendung übermittelt. Für diese Nachrichten werden einige Ergebnisse der Sicherheitsüberprüfung als Nachrichteneigenschaften angefügt, und die Anwendung kann diese Eigenschaften extrahieren und untersuchen, um zusätzliche Schritte wie Autorisierungsprüfungen auszuführen.


Die [**Funktion WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) kann verwendet werden, um eine der sicherheitsbezogenen Eigenschaften abzurufen, die in [**WS \_ MESSAGE PROPERTY \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)definiert sind. **WsGetMessageProperty** gibt einen Fehler für Abfragen zurück, bei denen Sicherheitseigenschaften abgefragt werden, die nicht auf den im Kanal verwendeten Sicherheitstyp anwendbar sind. Die Nachricht besitzt weiterhin die eigenschaften, die von der Abfragefunktion zurückgegeben werden.

Die folgenden API-Elemente werden mit Sicherheitsverarbeitungsergebnissen verwendet.

| Enumeration                                                                | Beschreibung                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ \_ \_ WS-SICHERHEITSTOKEN-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Definiert die Schlüssel für die Felder und Eigenschaften, die aus einem Sicherheitstoken extrahiert werden können. |



 



| Funktion                                                         | BESCHREIBUNG                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrahiert ein Feld oder eine Eigenschaft aus einem Sicherheitstoken. |



 



| Handle                                       | BESCHREIBUNG                                     |
|----------------------------------------------|-------------------------------------------------|
| [\_ \_ WS-SICHERHEITSTOKEN](ws-security-token.md) | Ein nicht transparentes Handle, das ein Sicherheitstoken darstellt. |



 

 

 




