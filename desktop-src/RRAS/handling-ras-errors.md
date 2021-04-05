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
# <a name="handling-ras-errors"></a><span data-ttu-id="42912-104">Behandeln von RAS-Fehlern</span><span class="sxs-lookup"><span data-stu-id="42912-104">Handling RAS Errors</span></span>

<span data-ttu-id="42912-105">Wenn ein Fehler auftritt, ruft der RAS-Verbindungs-Manager den Benachrichtigungs Handler des Clients auf.</span><span class="sxs-lookup"><span data-stu-id="42912-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="42912-106">Die Benachrichtigung gibt den Verbindungsstatus an, wenn der Fehler aufgetreten ist, und einen Code, der den Fehler identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42912-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="42912-107">In diesen Fällen sollte der Benachrichtigungs Handler [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) zum Beenden der RAS-Verbindung anrufen.</span><span class="sxs-lookup"><span data-stu-id="42912-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="42912-108">Die Fehlercodes, die RAS-Fehler identifizieren, werden in der Datei raserror. h definiert.</span><span class="sxs-lookup"><span data-stu-id="42912-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="42912-109">Der RAS-Client kann mit der Funktion " [**rasgeterrorstring**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) " eine Anzeige Zeichenfolge zum Beschreiben des Fehlers erhalten.</span><span class="sxs-lookup"><span data-stu-id="42912-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="42912-110">Eine Beschreibung dieser Fehler finden Sie unter [Routing-und Remote Zugriffs-Fehler Codes](routing-and-remote-access-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="42912-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




