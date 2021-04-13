---
title: Dynamische Authentifizierungs Konfiguration
description: Anwendungen können Authentifizierungs Konfigurationen für eine URL-Gruppe oder Server Sitzung jederzeit ändern.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309488"
---
# <a name="dynamic-authentication-configuration"></a>Dynamische Authentifizierungs Konfiguration

Standardmäßig führt die HTTP-Server-API keine Authentifizierung aus, es sei denn, Sie wird von der Anwendung ausdrücklich aktiviert. Anwendungen können Authentifizierungs Konfigurationen für eine URL-Gruppe oder Server Sitzung jederzeit ändern. Änderungen an der Authentifizierungs Konfiguration wirken sich nicht auf Anforderungen aus, die bereits authentifiziert sind oder an die Anwendung gesendet werden.

Für Authentifizierungs Schemas, in denen mehrere Schlag runden erforderlich sind, löscht die HTTP-Server-API den Authentifizierungs Hand Shake, wenn das aktuelle Schema aufgrund von Konfigurationsänderungen von der Anwendung nicht mehr unterstützt wird. Wenn die Anwendung z. b. das Aushandeln und Deaktivieren von NTLM ermöglicht und die HTTP-Server-API den zwischengeschalteten Authentifizierungs Handshake für NTLM hat, wird der Handshake für NTLM verworfen, und die Anforderung wird an die Anwendung übermittelt. Die Anwendung sendet eine 401-Authentifizierungs Aufforderung mit den neuen Authentifizierungs Typen, die im WWW-Authenticate-Header angegeben werden.

 

 




