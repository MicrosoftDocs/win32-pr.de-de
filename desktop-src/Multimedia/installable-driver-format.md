---
title: Installier bares Treiber Format
description: Installier bares Treiber Format
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- installierbare Treiber, Formate
- installierbare Treiber, driverproc-Funktion
- installierbare Treiber, Meldungen
- Treiber Meldungen
- Treiber Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314955"
---
# <a name="installable-driver-format"></a><span data-ttu-id="9490a-108">Installier bares Treiber Format</span><span class="sxs-lookup"><span data-stu-id="9490a-108">Installable Driver Format</span></span>

<span data-ttu-id="9490a-109">Jeder installierbare Treiber exportiert eine [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9490a-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="9490a-110">Diese allgemeine Einstiegspunkt Funktion empfängt *Treiber Nachrichten* vom System, die den Treiber dazu leiten, Aktionen auszuführen oder Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9490a-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="9490a-111">Das System sendet Treiber Nachrichten an die Funktion " **driverproc** ", wenn eine Anwendung oder dll den Treiber öffnet oder schließt oder wenn Sie anfordert, dass eine Nachricht an den Treiber gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9490a-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="9490a-112">Die **driverproc** -Funktion verarbeitet entweder die Nachricht oder übergibt die Nachricht an den Standard Nachrichten Handler, die [defdriverproc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9490a-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="9490a-113">In beiden Fällen muss von **driverproc** ein Wert zurückgegeben werden, der angibt, ob die angeforderte Aktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9490a-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 