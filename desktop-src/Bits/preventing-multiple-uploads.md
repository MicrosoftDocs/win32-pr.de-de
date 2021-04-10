---
title: Verhindern mehrerer Uploads
description: Beim Hochladen einer Datei erstellt Bits eine Sitzungs-ID, die die Uploadsitzung sowohl für den Bits-Client als auch den BITS-Server identifiziert.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036411"
---
# <a name="preventing-multiple-uploads"></a>Verhindern mehrerer Uploads

Beim Hochladen einer Datei erstellt Bits eine Sitzungs-ID, die die Uploadsitzung sowohl für den Bits-Client als auch den BITS-Server identifiziert. Wenn die Verbindung zwischen dem BITS-Client und dem Server getrennt wird, während Bits eine Datei hochlädt, verwendet der Client die Sitzungs-ID, um den Upload fortzusetzen.

Wenn der BITS-Client wie zuvor mit dem gleichen Server verbunden ist, erkennt der Server die Sitzungs-ID, und der Upload wird vom Zeitpunkt der Unterbrechung fortgesetzt. Wenn der Client jedoch eine Verbindung mit einem anderen Server herstellt, muss der Client den Upload von Anfang an starten, da der neue Server nicht über den Sitzungs Kontext oder die zuvor hochgeladenen Daten verfügt. Bits können sich mit einem anderen Server verbinden, wenn der BITS-Server in einer Webfarm gehostet wird und die BITS-IIS-Erweiterungs Eigenschaft [bitshostid](bits-iis-extension-properties.md)nicht festgelegt ist. Die bitshostid-Eigenschaft verhindert Neustarts, indem der BITS-Client gezwungen wird, eine Verbindung mit der eindeutigen Adresse des vorherigen Servers anstelle der freigegebenen Server Adresse herzustellen.

Der BITS-Server versucht, die Uploaddatei nur einmal an die Serveranwendung zu senden, aber es ist möglich, dass die Datei mehrmals gesendet wird. Dies kann z. b. der Fall sein, wenn der BITS-Server die Datei an die Serveranwendung sendet und dann beendet wird, während auf die Antwort von der Serveranwendung gewartet wird. Der BITS-Client empfängt einen Fehlercode von der HTTP-Ebene, und wiederholen Sie den Upload nach einer Verzögerung. Wenn der Server länger als das [bitshostidfallbacktimeout](bits-iis-extension-properties.md) -Timeout offline bleibt, sendet der Client die Anforderung schließlich erneut an die freigegebene Server Adresse. ein anderer BITS-Server empfängt die Datei und stellt Sie erneut an die Serveranwendung bereit.

Ein ähnlicher Fall kann auch mit einem einzelnen Front-End-Server auftreten. Wenn der Client z. b. die gesamte Datei auf den Server hochgeladen hat, bewirkt der endgültige Block, dass der Server die Datei an die Serveranwendung weitergibt. Wenn der BITS-Server oder die Serveranwendung beendet wird, nachdem die Datei verarbeitet wurde, aber bevor die Bestätigung an den Client gesendet wird, empfängt der Client einen Fehlercode und versucht ihn später erneut. Wenn der Client erneut versucht, wird dem BITS-Server angezeigt, dass der endgültige Block hochgeladen wurde, und die Datei wird erneut an die Serveranwendung weitergegeben. Wenn das mehrfache empfangen der Uploaddatei ein Problem für die Serveranwendung ist, sollten Sie in Erwägung gezogen, einen Transaktions Bezeichner in die Daten einzubeziehen.

 

 




