---
description: Ein Zeit Anbieter wird als dll implementiert. Jede DLL kann mehrere Zeit Anbieter unterstützen. Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Erstellen eines Zeit Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354868"
---
# <a name="creating-a-time-provider"></a>Erstellen eines Zeit Anbieters

Ein Zeit Anbieter wird als dll implementiert. Jede DLL kann mehrere Zeit Anbieter unterstützen. Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.

Zeit Anbieter müssen die folgenden Rückruf Funktionen implementieren:

-   [**Timeprovclose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**Timeprovcommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**Timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Nachdem die Anbieter-DLL geladen wurde, ruft der Zeit Anbieter-Manager [**timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)auf und übergibt den Namen des Anbieters und Zeiger auf die folgenden Funktionen:

-   [**Alertsamplesavailfunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**Gettimesysinfofunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**Logtimeproveventfunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Diese Funktionen sind für die Verwendung durch den Zeit Anbieter vorgesehen. Der Zeit Anbieter verwendet [**timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) , um ein Anbieter handle zurückzugeben, das der Zeit Anbieter-Manager beim Senden von Befehlen an den Zeit Anbieter verwendet. Der Handle-Wert wird durch den Zeit Anbieter definiert und wird hauptsächlich verwendet, um zwischen verschiedenen Anbietern zu unterscheiden, die in derselben dll implementiert werden. Der Zeit Anbieter kann mit [**logtimeproveventfunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)bedeutende Ereignisse protokollieren.

Der Zeit Anbieter-Manager verwendet [**timeprovcommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) zum Senden von Befehlen an den Zeit Anbieter. Wenn der Zeit Anbieter den Zeit Anbieter-Manager benachrichtigen muss, dass Zeit Beispiele verfügbar sind, wird [**alertsamplesavailfunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)aufgerufen. Der Zeit Anbieter-Manager ruft dann **timeprovcommand** mit dem TPC \_ getSamples-Befehl auf, um die Zeit Beispiele abzurufen. Es kann bis zu 16 Sekunden dauern, bis der Zeit Anbieter-Manager das Beispiel anfordert. Daher sollte die Anwendung nicht auf die Anforderung warten.

Um die Genauigkeit zu gewährleisten, sollte der Zeit Anbieter alle zeitbezogenen Informationen mithilfe von [**gettimesysinfofunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)abrufen.

Wenn der Zeit Anbieter heruntergefahren werden soll, ruft der Zeit Anbieter-Manager [**timeprovclose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)auf.

 

 



