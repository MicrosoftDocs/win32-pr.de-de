---
title: Informationen zur HTTP-Server-API
description: Die HTTP-Server-API bietet Entwicklern eine low-level-Schnittstelle zur Serverseite der HTTP-Funktionalität, wie in RFC 2616 definiert.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- HTTP-Server-API, Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55883fa75b366a2f5c5ef434f1eef3a95651440738735b025cfe5ef1b0534106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015008"
---
# <a name="about-http-server-api"></a>Informationen zur HTTP-Server-API

Die HTTP-Server-API bietet Entwicklern eine schnittstelle auf niedriger Ebene zur Serverseite der HTTP-Funktionalität, wie in [RFC 2616 definiert.](https://www.ietf.org/rfc/rfc2616.txt) Mit der API kann eine Anwendung HTTP-Anforderungen empfangen, die an URLs geleitet werden, und HTTP-Antworten senden. Zum Senden dynamischer Antworten wird die ISAPI- oder ASP.NET empfohlen.

Mit der HTTP-Server-API können mehrere Anwendungen auf einem System gleichzeitig verwendet werden, derselbe TCP-Port (z. B. Port 80 für HTTP oder Port 443 für HTTPS) gemeinsam verwendet und verschiedene Teile des URL-Namespace bereitgestellt werden.

Die HTTP-Server-API erfordert Kenntnisse der Programmiersprache C und Kenntnisse Windows API-Programmierung. Anwendungen, die keinen Zugriff auf HTTP auf niedriger Ebene erfordern, sollten die IIS-ISAPI oder die .NET Framework klassen für HTTP-basierte Lösungen verwenden.

 

 




