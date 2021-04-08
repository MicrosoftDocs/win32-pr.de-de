---
title: Behandeln von Server Anwendungsfehlern
description: Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet hat, sollte die Anwendung 200 zurückgeben.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707854"
---
# <a name="handling-server-application-errors"></a>Behandeln von Server Anwendungsfehlern

Wenn die Serveranwendung die hochgeladene Datei erfolgreich verarbeitet hat, sollte die Anwendung 200 zurückgeben. Wenn die Anwendung nicht 200 zurückgibt, verwendet der BITS-Client den Fehlercode, um zu ermitteln, ob der Fehler ein vorübergehender Fehler oder ein schwerwiegender Fehler ist.

Alle 3xx-Fehlercodes sind vorübergehende Fehler außer 300-305 und 307, bei denen es sich um schwerwiegende Fehler handelt. Alle 4xx-Fehlercodes sind schwerwiegende Fehler, außer 408 und 409, bei denen es sich um vorübergehende Fehler handelt. Alle 5xx-Fehlercodes sind vorübergehende Fehler außer 501 und 505, bei denen es sich um schwerwiegende Fehler handelt. Alle anderen HTTP-Codes werden als vorübergehende Fehler betrachtet. Beachten Sie, dass der Fehlercode 403 der einzige Fehlercode ist, der verhindert, dass Bits die Uploaddatei erneut an die Serveranwendung übermitteln.

Um den Fehler abzurufen, rufen Sie die [**ibackgroundcopyerror:: getError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) -Methode auf. Der Fehler Kontext ist eine BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung.

 

 




