---
title: Behandeln von Serveranwendungsfehlern
description: Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet, sollte die Anwendung 200 zurückgeben.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c66654bdc0070bf5988d16ac2489d62dc3614b44156337747052df5c7c314e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005280"
---
# <a name="handling-server-application-errors"></a>Behandeln von Serveranwendungsfehlern

Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet, sollte die Anwendung 200 zurückgeben. Wenn die Anwendung nicht 200 zurück gibt, ermittelt der BITS-Client mit dem Fehlercode, ob es sich bei dem Fehler um einen vorübergehenden oder schwerwiegenden Fehler handelt.

Alle 3xx-Fehlercodes sind vorübergehende Fehler mit Ausnahme von 300 bis 305 und 307, die schwerwiegende Fehler sind. Alle 4xx-Fehlercodes sind schwerwiegende Fehler, mit Ausnahme von 408 und 409, bei denen es sich um vorübergehende Fehler handelt. Alle 5xx-Fehlercodes sind vorübergehende Fehler mit Ausnahme von 501 und 505, die schwerwiegende Fehler sind. Alle anderen HTTP-Codes gelten als vorübergehende Fehler. Beachten Sie, dass ein 403-Fehlercode der einzige Fehlercode ist, der verhindert, dass BITS die Uploaddatei erneut an die Serveranwendung sendet.

Rufen Sie zum Abrufen des Fehlers die [**IBackgroundCopyError::GetError-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) auf. Der Fehlerkontext ist BG \_ ERROR \_ CONTEXT REMOTE \_ \_ APPLICATION.

 

 




