---
description: Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Asynchrone Druck Benachrichtigungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759558"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="8080c-103">Asynchrone Druck Benachrichtigungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8080c-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="8080c-104">Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.</span><span class="sxs-lookup"><span data-stu-id="8080c-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8080c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8080c-105">In this section</span></span>



| <span data-ttu-id="8080c-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8080c-106">Interface</span></span>                                                                     | <span data-ttu-id="8080c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8080c-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8080c-108">**Iprintasyncnotifycallback**</span><span class="sxs-lookup"><span data-stu-id="8080c-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="8080c-109">Erstellt und verwaltet einen Kommunikationskanal, der von Anwendungen und Komponenten verwendet wird, die vom Druck Spooler gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="8080c-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="8080c-110">**Iprintasyncnotifychannel**</span><span class="sxs-lookup"><span data-stu-id="8080c-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="8080c-111">Stellt einen Kommunikationskanal dar, den Komponenten, die vom Druck Spooler gehostet werden, zum Senden von Benachrichtigungen an Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8080c-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="8080c-112">Wenn der Kanal bidirektional ist, können Anwendungen den gleichen Kanal verwenden, um Antworten zurück an die Komponente zu senden.</span><span class="sxs-lookup"><span data-stu-id="8080c-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="8080c-113">**Iprintasyncnotifydataobject**</span><span class="sxs-lookup"><span data-stu-id="8080c-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="8080c-114">Kapselt die Daten, die in einem Benachrichtigungs Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8080c-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




