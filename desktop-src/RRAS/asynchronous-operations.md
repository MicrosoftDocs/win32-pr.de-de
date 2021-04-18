---
title: Asynchrone Vorgänge
description: Wenn "rasdial" als asynchroner Vorgang aufgerufen wird, gibt die Funktion sofort zurück.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388422"
---
# <a name="asynchronous-operations"></a>Asynchrone Vorgänge

Wenn " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " als asynchroner Vorgang aufgerufen wird, gibt die Funktion sofort zurück. Im asynchronen Modus muss der **rasdial** -Aufruf einen [Benachrichtigungs Handler](notification-handlers.md) angeben, den der RAS-Verbindungs-Manager verwendet, um den Client zu informieren, wenn der Verbindungsvorgang den Status ändert oder ein Fehler auftritt.

Der Benachrichtigungs Handler kann ein Fenster zum Empfangen von Nachrichten oder eine " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)", " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)" oder " [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) "-Rückruffunktion sein. Der RAS-Verbindungs-Manager führt seine asynchronen Benachrichtigungen im Kontext des Threads aus, der den [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl durchgeführt hat. Aus diesem Grund darf der aufrufende Thread erst beendet werden, wenn der Verbindungsvorgang erfolgreich ausgeführt wurde oder ein Fehler auftritt. Die Client Anwendung kann wie im synchronen Modus sicher beendet werden, sobald die Verbindung hergestellt wurde, und Sie muss [den Verbindungsvorgang](disconnecting.md) beenden, wenn ein Fehler auftritt.

 

 




