---
title: Dynamische Authentifizierungskonfiguration
description: Anwendungen können Authentifizierungskonfigurationen in einer URL-Gruppe oder Serversitzung jederzeit ändern.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014838"
---
# <a name="dynamic-authentication-configuration"></a>Dynamische Authentifizierungskonfiguration

Standardmäßig führt die HTTP-Server-API keine Authentifizierung durch, es sei denn, die Anwendung aktiviert sie ausdrücklich. Anwendungen können Authentifizierungskonfigurationen in einer URL-Gruppe oder Serversitzung jederzeit ändern. Änderungen an der Authentifizierungskonfiguration wirken sich nicht auf Anforderungen aus, die bereits authentifiziert oder an die Anwendung gesendet werden.

Bei Authentifizierungsschemas, bei denen mehrere Handshake-Runden erforderlich sind, löscht die HTTP-Server-API den Authentifizierungshandshake, wenn das aktuelle Schema aufgrund von Konfigurationsänderungen von der Anwendung nicht mehr unterstützt wird. Wenn die Anwendung beispielsweise Negotiate aktiviert und NTLM deaktiviert und sich die HTTP-Server-API im Zwischenauthentifizierungshandshake für NTLM befindet, wird der Handshake für NTLM verworfen, und die Anforderung wird an die Anwendung übergeben. Die Anwendung sendet eine 401-Authentifizierungsaufforderung mit den neuen Authentifizierungstypen, die im WWW-Authenticate-Header angegeben sind.

 

 




