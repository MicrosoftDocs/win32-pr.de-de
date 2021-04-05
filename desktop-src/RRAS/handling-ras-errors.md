---
title: Behandeln von RAS-Fehlern
description: Wenn ein Fehler auftritt, ruft der RAS-Verbindungs-Manager den Benachrichtigungs Handler des Clients auf.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS-Dienst (RAS), Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712869"
---
# <a name="handling-ras-errors"></a>Behandeln von RAS-Fehlern

Wenn ein Fehler auftritt, ruft der RAS-Verbindungs-Manager den Benachrichtigungs Handler des Clients auf. Die Benachrichtigung gibt den Verbindungsstatus an, wenn der Fehler aufgetreten ist, und einen Code, der den Fehler identifiziert. In diesen Fällen sollte der Benachrichtigungs Handler [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) zum Beenden der RAS-Verbindung anrufen.

Die Fehlercodes, die RAS-Fehler identifizieren, werden in der Datei raserror. h definiert. Der RAS-Client kann mit der Funktion " [**rasgeterrorstring**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) " eine Anzeige Zeichenfolge zum Beschreiben des Fehlers erhalten. Eine Beschreibung dieser Fehler finden Sie unter [Routing-und Remote Zugriffs-Fehler Codes](routing-and-remote-access-error-codes.md) .

 

 




