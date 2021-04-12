---
title: Informationen zur HTTP-Server-API
description: Die HTTP-Server-API stellt Entwicklern eine Low-Level-Schnittstelle der Server Seite der HTTP-Funktionalität bereit, die in RFC 2616 definiert ist.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- HTTP-Server-API, Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389951"
---
# <a name="about-http-server-api"></a>Informationen zur HTTP-Server-API

Die HTTP-Server-API stellt Entwicklern eine Low-Level-Schnittstelle der Server Seite der HTTP-Funktionalität bereit, die in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)definiert ist. Die API ermöglicht es einer Anwendung, HTTP-Anforderungen an URLs zu empfangen und HTTP-Antworten zu senden. Zum Senden dynamischer Antworten werden die ISAPI-oder ASP.NET-Schnittstellen empfohlen.

Die HTTP-Server-API ermöglicht die Koexistenz mehrerer Anwendungen auf einem System, wobei derselbe TCP-Port (z. b. Port 80 für http oder Port 443 für HTTPS) und verschiedene Teile des URL-Namespace verwendet werden.

Die HTTP-Server-API erfordert Kenntnisse über die Programmiersprache C und eine Vertrautheit mit der Windows-API-Programmierung. Anwendungen, die keinen Low-Level-Zugriff auf http benötigen, sollten die IIS-ISAPI oder die .NET Framework Klassen für HTTP-basierte Lösungen verwenden.

 

 




