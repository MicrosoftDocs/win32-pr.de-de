---
title: Auswerten von Ausnahmen
description: Die HTTP-Server-API stellt Registrierungsschlüssel zur Verfügung, um das Durchsuchen von Ausnahmen zur HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Auswerten von Ausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947824"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="3a4cd-104">Auswerten von Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="3a4cd-104">Parsing Exceptions</span></span>

<span data-ttu-id="3a4cd-105">Die HTTP-Server-API stellt Registrierungsschlüssel zur Verfügung, um das Durchsuchen von Ausnahmen zur HTTP/1.1-Spezifikation aus Gründen der Abwärtskompatibilität</span><span class="sxs-lookup"><span data-stu-id="3a4cd-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="3a4cd-106">Diese Ausnahmen sind nicht standardmäßig aktiviert und sollten nur für die Fall Weise aktiviert werden, wenn auf dem Server Kompatibilitätsprobleme mit HTTP-Clients auftreten.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="3a4cd-107">Diese Werte werden unter folgendem Registrierungs Speicherort erstellt:</span><span class="sxs-lookup"><span data-stu-id="3a4cd-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="3a4cd-108">In der folgenden Tabelle sind die zur Unterstützung der aufgeführten Ausnahmen angegebenen Registrierungsschlüssel aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="3a4cd-109">Legen Sie zum Aktivieren einer Ausnahme den entsprechenden Schlüsselwert auf 1 fest, und starten Sie den HTTP-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="3a4cd-110">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="3a4cd-110">Key name</span></span>                              | <span data-ttu-id="3a4cd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a4cd-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4cd-112">Allowweakheadernamesyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="3a4cd-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="3a4cd-113">Ermöglicht dem http-Parser das akzeptieren von Header Namen mit Trennzeichen wie z. b. "?".</span><span class="sxs-lookup"><span data-stu-id="3a4cd-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3a4cd-114">Allowweakheadervaluesyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="3a4cd-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="3a4cd-115">Ermöglicht dem http-Parser das akzeptieren von Header Werten mit unformatierten (ohne Escapezeichen) Steuerzeichen.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3a4cd-116">Allowcaseinsensitiveverbs (DWORD)</span><span class="sxs-lookup"><span data-stu-id="3a4cd-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="3a4cd-117">Ermöglicht es dem http-Parser, HTTP-Methoden/-Verben wie "Get" in Kleinbuchstaben zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3a4cd-118">"Zugewunescapedrestrictedchars" (DWORD)</span><span class="sxs-lookup"><span data-stu-id="3a4cd-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="3a4cd-119">Ermöglicht es dem http-Parser, Steuerzeichen in abspath und Abfrage Zeichenfolgen der URL zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="3a4cd-120">Im Fall einer absolute URL werden Steuerzeichen im Hostnamen nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="3a4cd-121">Alle URLs von URLs, nämlich UTF8, DBCS und ANSI, lassen Steuerzeichen zu.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="3a4cd-122">Alle ASCII-Steuerzeichen mit Ausnahme von NUL (0x00), LF (0x0A), CR (0x0D) und horizontaler Registerkarte (0x09) sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="3a4cd-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




