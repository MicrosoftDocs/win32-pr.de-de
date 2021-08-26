---
title: Asynchrone Vorgänge
description: Wenn RasDial als asynchroner Vorgang aufgerufen wird, gibt die Funktion sofort zurück.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db03b1d9d3c98e84bc9a2f4fd80ec7206d9a4524608cdbc96cca83f89d0ea00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030560"
---
# <a name="asynchronous-operations"></a>Asynchrone Vorgänge

Wenn [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) als asynchroner Vorgang aufgerufen wird, gibt die Funktion sofort zurück. Im asynchronen Modus muss der **RasDial-Aufruf** einen [Benachrichtigungshandler](notification-handlers.md) angeben, den der Remotezugriff Verbindungs-Manager verwendet, um den Client zu informieren, wenn sich der Status des Verbindungsvorgangs ändert oder ein Fehler auftritt.

Der Benachrichtigungshandler kann ein Fenster zum Empfangen von Nachrichten oder eine [**RasDialFunc-,**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) [**RasDialFunc1-**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)oder [**RasDialFunc2-Rückruffunktion**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) sein. Der Remotezugriffs-Verbindungs-Manager nimmt seine asynchronen Benachrichtigungen im Kontext des Threads vor, der den [**RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) durchgeführt hat. Aus diesem Grund darf der aufrufende Thread erst beendet werden, wenn der Verbindungsvorgang erfolgreich hergestellt wurde oder ein Fehler auftritt. Wie im synchronen Modus kann die Clientanwendung sicher beendet werden, sobald die Verbindung hergestellt wurde, und sie muss [den Verbindungsvorgang beenden,](disconnecting.md) wenn ein Fehler auftritt.

 

 




