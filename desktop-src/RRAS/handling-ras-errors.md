---
title: Behandeln von RAS-Fehlern
description: Wenn ein Fehler auftritt, ruft der Remotezugriff Verbindungs-Manager den Benachrichtigungshandler des Clients auf.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS des Ras-Diensts, Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b870678eb2dbe95c190bc67415b9abb5481c33918429194404893349c0d7f7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791278"
---
# <a name="handling-ras-errors"></a>Behandeln von RAS-Fehlern

Wenn ein Fehler auftritt, ruft der Remotezugriff Verbindungs-Manager den Benachrichtigungshandler des Clients auf. Die Benachrichtigung gibt den Verbindungsstatus an, wenn der Fehler aufgetreten ist, und einen Code, der den Fehler identifiziert. In diesen Fällen sollte der Benachrichtigungshandler [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) aufrufen, um die RAS-Verbindung zu beenden.

Die Fehlercodes, die RAS-Fehler identifizieren, werden in der Datei raserror.h definiert. Der RAS-Client kann die [**RasGetErrorString-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) verwenden, um eine Anzeigezeichenfolge abzurufen, die den Fehler beschreibt. Eine Beschreibung dieser Fehler finden Sie unter Fehlercodes für [Routing und Remotezugriff.](routing-and-remote-access-error-codes.md)

 

 




