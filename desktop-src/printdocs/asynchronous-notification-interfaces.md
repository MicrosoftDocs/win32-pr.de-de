---
description: Erfahren Sie mehr über Schnittstellen, die in der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet werden, die vom Druckspooler gehostet werden.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Benachrichtigungsschnittstellen für asynchrones Drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396095"
---
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="1a69e-103">Benachrichtigungsschnittstellen für asynchrones Drucken</span><span class="sxs-lookup"><span data-stu-id="1a69e-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="1a69e-104">Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druckspooler gehostet werden, z. B. Druckertreiber und Portmonitore.</span><span class="sxs-lookup"><span data-stu-id="1a69e-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a69e-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1a69e-105">In this section</span></span>



| <span data-ttu-id="1a69e-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1a69e-106">Interface</span></span>                                                                     | <span data-ttu-id="1a69e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a69e-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a69e-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="1a69e-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="1a69e-109">Erstellt und verwaltet einen Kommunikationskanal, der von Anwendungen und Komponenten verwendet wird, die vom Druckspooler gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="1a69e-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="1a69e-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="1a69e-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="1a69e-111">Stellt einen Kommunikationskanal dar, den komponenten, die vom Druckspooler gehostet werden, zum Senden von Benachrichtigungen an Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a69e-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="1a69e-112">Wenn der Kanal bidirektional ist, können Anwendungen denselben Kanal verwenden, um Antworten zurück an die Komponente zu senden.</span><span class="sxs-lookup"><span data-stu-id="1a69e-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="1a69e-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="1a69e-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="1a69e-114">Kapselt die in einem Benachrichtigungskanal gesendeten Daten.</span><span class="sxs-lookup"><span data-stu-id="1a69e-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




