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
# <a name="asynchronous-operations"></a><span data-ttu-id="1dc30-103">Asynchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="1dc30-103">Asynchronous Operations</span></span>

<span data-ttu-id="1dc30-104">Wenn " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " als asynchroner Vorgang aufgerufen wird, gibt die Funktion sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="1dc30-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as an asynchronous operation, the function returns immediately.</span></span> <span data-ttu-id="1dc30-105">Im asynchronen Modus muss der **rasdial** -Aufruf einen [Benachrichtigungs Handler](notification-handlers.md) angeben, den der RAS-Verbindungs-Manager verwendet, um den Client zu informieren, wenn der Verbindungsvorgang den Status ändert oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1dc30-105">In asynchronous mode, the **RasDial** call must specify a [notification handler](notification-handlers.md) that the Remote Access Connection Manager uses to inform the client whenever the connection operation changes states or an error occurs.</span></span>

<span data-ttu-id="1dc30-106">Der Benachrichtigungs Handler kann ein Fenster zum Empfangen von Nachrichten oder eine " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)", " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)" oder " [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) "-Rückruffunktion sein.</span><span class="sxs-lookup"><span data-stu-id="1dc30-106">The notification handler can be a window to receive messages, or a [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1), or [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) callback function.</span></span> <span data-ttu-id="1dc30-107">Der RAS-Verbindungs-Manager führt seine asynchronen Benachrichtigungen im Kontext des Threads aus, der den [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="1dc30-107">The Remote Access Connection Manager makes its asynchronous notifications in the context of the thread that made the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span> <span data-ttu-id="1dc30-108">Aus diesem Grund darf der aufrufende Thread erst beendet werden, wenn der Verbindungsvorgang erfolgreich ausgeführt wurde oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1dc30-108">For this reason, the calling thread must not terminate until the connection operation has been successfully established or an error occurs.</span></span> <span data-ttu-id="1dc30-109">Die Client Anwendung kann wie im synchronen Modus sicher beendet werden, sobald die Verbindung hergestellt wurde, und Sie muss [den Verbindungsvorgang](disconnecting.md) beenden, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1dc30-109">As in synchronous mode, the client application can safely terminate once the connection has been established, and it must [shut down the connection operation](disconnecting.md) if an error occurs.</span></span>

 

 




