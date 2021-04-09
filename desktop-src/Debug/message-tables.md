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
# <a name="message-tables"></a>Nachrichten Tabellen

Nachrichten Tabellen sind spezielle Zeichen folgen Ressourcen, die beim Anzeigen von Fehlermeldungen verwendet werden. Sie werden in einer Ressourcen Datei mit der [messagetable](../menurc/messagetable-resource.md) -Ressourcen Definitions Anweisung deklariert. Verwenden Sie zum Zugreifen auf die Meldungs Zeichenfolgen die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion.

Das System stellt eine Nachrichten Tabelle für die [Systemfehler Codes](system-error-codes.md)bereit. Zum Abrufen der Zeichenfolge, die dem Fehlercode entspricht, rufen Sie [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem \_ Flag Format Message \_ from System auf \_ .

Befolgen Sie die Anweisungen in [Nachrichten Text Dateien](../eventlog/message-text-files.md), um eine Nachrichten Tabelle für Ihre Anwendung bereitzustellen. Um Zeichen folgen aus der Nachrichten Tabelle abzurufen, rufen Sie [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem \_ Flag Format Message \_ from \_ HMODULE auf.

 

 
