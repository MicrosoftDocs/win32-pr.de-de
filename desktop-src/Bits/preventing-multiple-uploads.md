---
title: Verhindern mehrerer Uploads
description: Wenn Sie eine Datei hochladen, erstellt BITS eine Sitzungs-ID, die die Uploadsitzung sowohl auf den BITS-Client als auch auf den BITS-Server identifiziert.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c08555acf8bcdc99576675b0ec5852f322f7b37fea9821f3f0156352a29b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701700"
---
# <a name="preventing-multiple-uploads"></a>Verhindern mehrerer Uploads

Wenn Sie eine Datei hochladen, erstellt BITS eine Sitzungs-ID, die die Uploadsitzung sowohl auf den BITS-Client als auch auf den BITS-Server identifiziert. Wenn die Verbindung zwischen dem BITS-Client und dem Server unterbrochen wird, während BITS eine Datei hoch lädt, verwendet der Client die Sitzungs-ID, um den Upload wieder aufzunehmen.

Wenn der BITS-Client eine Verbindung mit dem gleichen Server wie zuvor herstellt, erkennt der Server die Sitzungs-ID, und der Upload wird ab dem Punkt der Unterbrechung fortgesetzt. Wenn der Client jedoch eine Verbindung mit einem anderen Server herstellt, muss der Client den Upload von Anfang an starten, da der neue Server nicht über den Sitzungskontext oder die zuvor hochgeladenen Daten verfügt. BITS kann eine Verbindung mit einem anderen Server herstellen, wenn der BITS-Server in einer Webfarm gehostet wird und die BITS IIS-Erweiterungseigenschaft [BITSHostId](bits-iis-extension-properties.md)nicht festgelegt ist. Die BITSHostId-Eigenschaft verhindert Neustarts, indem der BITS-Client gezwungen wird, anstelle der freigegebenen Serveradresse eine Verbindung mit der eindeutigen Adresse des vorherigen Servers herzustellen.

Der BITS-Server versucht, die Uploaddatei nur einmal an die Serveranwendung zu senden. Es ist jedoch möglich, dass die Datei mehr als einmal gesendet wird. Dies kann beispielsweise der Fall sein, wenn der BITS-Server die Datei an die Serveranwendung sendet und dann beendet wird, während auf die Antwort von der Serveranwendung gewartet wird. Der BITS-Client erhält einen Fehlercode von der HTTP-Ebene und wiederholen den Upload nach einer Verzögerung. Wenn der Server länger als das [BitsHostIdFallbackTimeout-Timeout](bits-iis-extension-properties.md) offline bleibt, sendet der Client die Anforderung schließlich erneut an die freigegebene Serveradresse. Ein anderer BITS-Server erhält die Datei und übermittelt sie erneut an die Serveranwendung.

Ein ähnlicher Fall kann auch bei einem einzelnen Front-End-Server auftreten. Wenn der Client z. B. die gesamte Datei auf den Server hochgeladen hat, bewirkt der letzte Block, dass der Server die Datei an die Serveranwendung weiter sendet. Wenn der BITS-Server oder die Serveranwendung beendet wird, nachdem die Datei verarbeitet wurde, aber bevor die Bestätigung an den Client gesendet wird, erhält der Client einen Fehlercode und wird später erneut versuchen. Wenn der Client einen erneuten Vorgang unterniert, sieht der BITS-Server, dass der letzte Block hochgeladen wurde, und die Datei wird erneut an die Serveranwendung weitergeleitet. Wenn der mehrfache Empfang der Uploaddatei ein Problem für Ihre Serveranwendung ist, sollten Sie in Erwägung ziehen, einen Transaktionsbezeichner in die Daten einzuladen.

 

 




