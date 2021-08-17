---
description: Ein Zeitanbieter wird als DLL implementiert. Jede DLL kann mehrere Zeitanbieter unterstützen. Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Erstellen eines Zeitanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58766bf0ed7339bf8c9bfd7abc7434ddc43165b7cbdd77bcfd5420947e743d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885763"
---
# <a name="creating-a-time-provider"></a>Erstellen eines Zeitanbieters

Ein Zeitanbieter wird als DLL implementiert. Jede DLL kann mehrere Zeitanbieter unterstützen. Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.

Zeitanbieter müssen die folgenden Rückruffunktionen implementieren:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Nachdem die Anbieter-DLL geladen wurde, ruft der Zeitanbieter-Manager [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)auf und überträgt den Namen des Anbieters und Zeiger auf die folgenden Funktionen:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Diese Funktionen sind für die Verwendung durch den Zeitanbieter. Der Zeitanbieter verwendet [**TimeProvOpen,**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) um ein Anbieterhand handle zurück zu geben, das der Zeitanbieter-Manager beim Senden von Befehlen an den Zeitanbieter verwendet. Der Handlewert wird vom Zeitanbieter definiert und hauptsächlich verwendet, um zwischen verschiedenen Anbietern zu unterscheiden, die in derselben DLL implementiert sind. Der Zeitanbieter kann wichtige Ereignisse mit [**LogTimeProvEventFunc protokollieren.**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Der Zeitanbieter-Manager verwendet [**TimeProvCommand,**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) um Befehle an den Zeitanbieter zu senden. Wenn der Zeitanbieter den Zeitanbieter-Manager benachrichtigen muss, dass Zeitbeispiele verfügbar sind, ruft er [**AlertSamplesAvailFunc auf.**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc) Der Zeitanbieter-Manager ruft **dann TimeProvCommand** mit dem TPC \_ GetSamples-Befehl auf, um die Zeitbeispiele abzurufen. Es kann bis zu 16 Sekunden dauern, bis der Anbieter-Manager das Beispiel anfing. Daher sollte die Anwendung nicht auf die Anforderung warten.

Um die Genauigkeit sicherzustellen, sollte der Zeitanbieter alle zeitbezogenen Informationen mit [**getTimeSysInfoFunc abrufen.**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)

Wenn der Zeitanbieter heruntergefahren werden soll, ruft der Zeitanbieter-Manager [**TimeProvClose auf.**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)

 

 



