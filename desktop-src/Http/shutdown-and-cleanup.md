---
title: Herunterfahren und Bereinigten
description: Damit eine Anwendung ordnungsgemäß beendet wird, muss sie die folgenden Bereinigungsvorgänge ausführen.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950690"
---
# <a name="shutdown-and-cleanup"></a>Herunterfahren und Bereinigten

Damit eine Anwendung ordnungsgemäß beendet wird, muss sie die folgenden Bereinigungsvorgänge ausführen:

-   Entfernen Sie alle registrierten URLs aus der URL-Gruppe, indem Sie die [**HttpRemoveUrlFromUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) aufrufen, um die Registrierung von URLs zu aufheben, die zuvor im Aufruf von [**HttpAddUrlToUrlGroup registriert wurden.**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)
-   Schließen Sie die URL-Gruppe, indem Sie die [**Funktion HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) aufrufen. Alle URL-Gruppen, die unter einer Serversitzung erstellt wurden, müssen geschlossen werden, bevor die Serversitzung geschlossen wird.
-   Schließen Sie die Serversitzung, indem Sie [**HttpCloseServerSession aufrufen.**](/windows/desktop/api/Http/nf-http-httpcloseserversession)
-   Schließen Sie das Handle für die Anforderungswarteschlange, indem Sie [**HttpCloseRequestQueue aufrufen.**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)
-   Beenden Sie die von der HTTP-Server-API erstellten Ressourcen, indem Sie die [**HttpTerminate-Funktion**](/windows/desktop/api/Http/nf-http-httpterminate) mit übereinstimmenden Flageinstellungen für jeden Aufruf aufrufen, den die Anwendung ursprünglich für [**HttpInitialize ausgeführt hat.**](/windows/desktop/api/Http/nf-http-httpinitialize) Jeder dieser Aufrufe beendet alle Ressourcen, die im Aufruf von [**HttpInitialize erstellt wurden.**](/windows/desktop/api/Http/nf-http-httpinitialize)

 

 




