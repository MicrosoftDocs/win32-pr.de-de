---
description: Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Asynchrone Druck Benachrichtigungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369033"
---
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="1bf97-103">Asynchrone Druck Benachrichtigungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1bf97-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="1bf97-104">Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.</span><span class="sxs-lookup"><span data-stu-id="1bf97-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1bf97-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1bf97-105">In this section</span></span>



| <span data-ttu-id="1bf97-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="1bf97-106">Function</span></span>                                                                                        | <span data-ttu-id="1bf97-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bf97-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bf97-108">**"Kreateprintasyncnotifychannel"**</span><span class="sxs-lookup"><span data-stu-id="1bf97-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="1bf97-109">Erstellt einen Kommunikationskanal zwischen einer Druckerspooler-gehosteten Druckkomponente, z. b. einem Druckertreiber oder Port Monitor, und einer Anwendung, die Benachrichtigungen von der Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="1bf97-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="1bf97-110">**Registerforprintasyncbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="1bf97-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="1bf97-111">Ermöglicht einer Anwendung das Registrieren für Benachrichtigungen von Druckerspooler-gehosteten Druckkomponenten wie Druckertreibern, Druck Prozessoren und Port Monitoren.</span><span class="sxs-lookup"><span data-stu-id="1bf97-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="1bf97-112">**Unregisterforprintasyncnotification**</span><span class="sxs-lookup"><span data-stu-id="1bf97-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="1bf97-113">Ermöglicht es einer Anwendung, die registriert hat, Benachrichtigungen von Druckkomponenten des Druck Spoolers zu empfangen, um die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="1bf97-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




