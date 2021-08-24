---
description: Nachrichtentabellen sind spezielle Zeichenfolgenressourcen, die beim Anzeigen von Fehlermeldungen verwendet werden. Sie werden in einer Ressourcendatei mithilfe der MESSAGETABLE-Ressourcendefinitions-Anweisung deklariert. Verwenden Sie die FormatMessage-Funktion, um auf die Nachrichtenzeichenfolgen zuzugreifen.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Meldungstabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691820"
---
# <a name="message-tables"></a>Meldungstabellen

Nachrichtentabellen sind spezielle Zeichenfolgenressourcen, die beim Anzeigen von Fehlermeldungen verwendet werden. Sie werden in einer Ressourcendatei mithilfe der MESSAGETABLE-Ressourcendefinitions-Anweisung deklariert. [](../menurc/messagetable-resource.md) Verwenden Sie die [**FormatMessage-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) um auf die Nachrichtenzeichenfolgen zuzugreifen.

Das System stellt eine Meldungstabelle für die [Systemfehlercodes bereit.](system-error-codes.md) Um die Zeichenfolge abzurufen, die dem Fehlercode entspricht, rufen [**Sie FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem FLAG FORMAT \_ MESSAGE FROM SYSTEM \_ \_ auf.

Um eine Meldungstabelle für Ihre Anwendung bereitzustellen, befolgen Sie die Anweisungen unter [Meldungstextdateien](../eventlog/message-text-files.md). Um Zeichenfolgen aus ihrer Nachrichtentabelle abzurufen, rufen [**Sie FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem Flag FORMAT \_ MESSAGE FROM \_ \_ HMODULE auf.

 

 
