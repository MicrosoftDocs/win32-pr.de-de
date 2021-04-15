---
title: Genaues Erfassungs Steuerelement
description: Genaues Erfassungs Steuerelement
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Avicap-Rückruf Funktionen, präzises Erfassungs Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515699"
---
# <a name="precise-capture-control"></a>Genaues Erfassungs Steuerelement

Ein Aufzeichnungs Fenster kann der Capture-Control-Rückruffunktion eine genaue Kontrolle über die Momente bieten, in denen die Erfassung von streamingvorhalten beginnt und endet. Die erste Meldung, die vom Aufzeichnungs Treiber an die Rückruf Prozedur gesendet wird, legt den *nState* -Parameter auf "controlcallback Preroll" fest, \_ nachdem alle Puffer zugeordnet wurden und alle anderen Aufzeichnungs Vorbereitungen vollständig sind. Diese Meldung gibt der Anwendung die Möglichkeit, die Videoquellen vorab zu überstehen. (Die Rückruffunktion gibt *nState* als zweiten Parameter an.) Die Rückruffunktion gibt dann zu dem Zeitpunkt zurück, zu dem die Aufzeichnung beginnt. Der Rückgabewert **true** von der Rückruffunktion setzt die Erfassung fort. Der Rückgabewert **false** bricht Capture ab. Sobald die Erfassung beginnt, wird die Rückruffunktion häufig aufgerufen, wobei *nState* auf controlcallback Capture festgelegt ist, \_ damit die Anwendung die Erfassung beenden kann, indem **false** zurückgegeben wird.

 

 




