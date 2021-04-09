---
description: Die meisten Get-und Set-Vorgänge behandeln nur eine Komponente von Informationen. Die phonegetstatus-Funktion gibt umfassende Statusinformationen zu einem Telefongerät an eine Anwendung zurück.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Status (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864999"
---
# <a name="status-telephony-api"></a><span data-ttu-id="73b22-104">Status (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="73b22-104">Status (Telephony API)</span></span>

<span data-ttu-id="73b22-105">Die meisten Get-und Set-Vorgänge behandeln nur eine Komponente von Informationen.</span><span class="sxs-lookup"><span data-stu-id="73b22-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="73b22-106">Die [**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) -Funktion gibt umfassende Statusinformationen zu einem Telefongerät an eine Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="73b22-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="73b22-107">Wie bereits erwähnt, wird bei jeder Änderung eines Status Elements auf dem Telefongerät eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendungsfunktion gesendet.</span><span class="sxs-lookup"><span data-stu-id="73b22-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="73b22-108">Zu den Parametern dieser Nachricht gehören ein Handle für das Telefongerät und ein Hinweis auf das geänderte Status Element.</span><span class="sxs-lookup"><span data-stu-id="73b22-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="73b22-109">Eine Anwendung kann [**phonesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) verwenden, um die spezifischen Statusänderungen auszuwählen, für die Sie benachrichtigt werden möchten.</span><span class="sxs-lookup"><span data-stu-id="73b22-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="73b22-110">Dementsprechend gibt [**phonegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) die Statusänderungen zurück, für die die Anwendung benachrichtigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73b22-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



