---
description: Nachrichten Tabellen sind spezielle Zeichen folgen Ressourcen, die beim Anzeigen von Fehlermeldungen verwendet werden. Sie werden in einer Ressourcen Datei mit der messagetable-Ressourcen Definitions Anweisung deklariert. Verwenden Sie zum Zugreifen auf die Meldungs Zeichenfolgen die FormatMessage-Funktion.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Nachrichten Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958191"
---
# <a name="message-tables"></a><span data-ttu-id="cc2eb-105">Nachrichten Tabellen</span><span class="sxs-lookup"><span data-stu-id="cc2eb-105">Message Tables</span></span>

<span data-ttu-id="cc2eb-106">Nachrichten Tabellen sind spezielle Zeichen folgen Ressourcen, die beim Anzeigen von Fehlermeldungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="cc2eb-107">Sie werden in einer Ressourcen Datei mit der [messagetable](../menurc/messagetable-resource.md) -Ressourcen Definitions Anweisung deklariert.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="cc2eb-108">Verwenden Sie zum Zugreifen auf die Meldungs Zeichenfolgen die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="cc2eb-109">Das System stellt eine Nachrichten Tabelle für die [Systemfehler Codes](system-error-codes.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="cc2eb-110">Zum Abrufen der Zeichenfolge, die dem Fehlercode entspricht, rufen Sie [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem \_ Flag Format Message \_ from System auf \_ .</span><span class="sxs-lookup"><span data-stu-id="cc2eb-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="cc2eb-111">Befolgen Sie die Anweisungen in [Nachrichten Text Dateien](../eventlog/message-text-files.md), um eine Nachrichten Tabelle für Ihre Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="cc2eb-112">Um Zeichen folgen aus der Nachrichten Tabelle abzurufen, rufen Sie [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem \_ Flag Format Message \_ from \_ HMODULE auf.</span><span class="sxs-lookup"><span data-stu-id="cc2eb-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
