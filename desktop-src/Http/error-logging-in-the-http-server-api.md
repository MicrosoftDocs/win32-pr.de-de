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
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="dc5a4-104">Fehlerprotokollierung in der HTTP-Server-API</span><span class="sxs-lookup"><span data-stu-id="dc5a4-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="dc5a4-105">Einige Arten von Fehlern werden von der HTTP-Server-API behandelt und nicht zur Verarbeitung an eine Anwendung zurückgegeben, da die Häufigkeit solcher Fehler andernfalls ein Ereignisprotokoll oder einen Anwendungs Handler überfluten könnte.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="dc5a4-106">In den folgenden drei Themen werden die unterschiedlichen Aspekte der HTTP-Server-API-Fehler Protokollierung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="dc5a4-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="dc5a4-107">[Konfiguration](configuring-http-server-api-error-logging.md) Registrierungs Einstellungen steuern, ob die HTTP-Server-API Fehler protokolliert, die maximal zulässige Größe der Protokolldateien und den Speicherort der Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="dc5a4-108">[Protokolldatei Format](format-of-the-http-server-api-error-logs.md) Die HTTP-Server-API erstellt Protokolldateien, die den W3C-Protokolldatei Konventionen (World Wide Web Consortium) entsprechen und mithilfe von Standard Tools analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="dc5a4-109">Im Gegensatz zu W3C-Protokolldateien enthalten http-Server-API-Protokolldateien jedoch keine Namen der Spalten.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="dc5a4-110">[Protokollierte Fehlertypen](types-of-errors-logged-by-the-http-server-api.md) Die HTTP-Server-API protokolliert eine Reihe von häufigen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




