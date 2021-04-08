---
title: Herunterfahren und bereinigen
description: Damit eine Anwendung ordnungsgemäß beendet wird, muss Sie die folgenden Bereinigungs Vorgänge ausführen.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037067"
---
# <a name="shutdown-and-cleanup"></a>Herunterfahren und bereinigen

Damit eine Anwendung ordnungsgemäß beendet wird, muss Sie die folgenden Bereinigungs Vorgänge ausführen:

-   Entfernen Sie alle registrierten URLs aus der URL-Gruppe, indem Sie die [**httpremoveurlfromurlgroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) -Funktion aufrufen, um die zuvor beim Aufruf von [**httpaddurltourlgroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)registrierten URLs aufzuheben.
-   Schließen Sie die URL-Gruppe, indem Sie die [**httpcloseurlgroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) -Funktion aufrufen. Alle URL-Gruppen, die unter einer Server Sitzung erstellt wurden, müssen vor dem Schließen der Server Sitzung geschlossen werden.
-   Schließen Sie die Server Sitzung, indem Sie [**httpcloseserversession**](/windows/desktop/api/Http/nf-http-httpcloseserversession)aufrufen.
-   Schließen Sie das Handle für die Anforderungs Warteschlange, indem Sie [**httpcloserequestqueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)aufrufen.
-   Beenden Sie die von der HTTP-Server-API erstellten Ressourcen, indem Sie die [**httpend**](/windows/desktop/api/Http/nf-http-httpterminate) -Funktion mit übereinstimmenden Flageinstellungen für jeden Aufruf der Anwendung aufrufen, die ursprünglich für [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)erstellt wurde. Jeder dieser Aufrufe beendet alle Ressourcen, die im Aufruf von [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)erstellt wurden.

 

 




