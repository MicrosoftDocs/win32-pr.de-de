---
title: Fehlerprotokollierung in der HTTP-Server-API
description: Einige Arten von Fehlern werden von der HTTP-Server-API behandelt und nicht zur Verarbeitung an eine Anwendung zurückgegeben, da die Häufigkeit solcher Fehler andernfalls ein Ereignisprotokoll oder einen Anwendungs Handler überfluten könnte.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- HTTP-Server-API, Fehler Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339192"
---
# <a name="error-logging-in-the-http-server-api"></a>Fehlerprotokollierung in der HTTP-Server-API

Einige Arten von Fehlern werden von der HTTP-Server-API behandelt und nicht zur Verarbeitung an eine Anwendung zurückgegeben, da die Häufigkeit solcher Fehler andernfalls ein Ereignisprotokoll oder einen Anwendungs Handler überfluten könnte.

In den folgenden drei Themen werden die unterschiedlichen Aspekte der HTTP-Server-API-Fehler Protokollierung beschrieben:

-   [Konfiguration](configuring-http-server-api-error-logging.md) Registrierungs Einstellungen steuern, ob die HTTP-Server-API Fehler protokolliert, die maximal zulässige Größe der Protokolldateien und den Speicherort der Protokolldateien.
-   [Protokolldatei Format](format-of-the-http-server-api-error-logs.md) Die HTTP-Server-API erstellt Protokolldateien, die den W3C-Protokolldatei Konventionen (World Wide Web Consortium) entsprechen und mithilfe von Standard Tools analysiert werden können. Im Gegensatz zu W3C-Protokolldateien enthalten http-Server-API-Protokolldateien jedoch keine Namen der Spalten.
-   [Protokollierte Fehlertypen](types-of-errors-logged-by-the-http-server-api.md) Die HTTP-Server-API protokolliert eine Reihe von häufigen Fehlern.

 

 




