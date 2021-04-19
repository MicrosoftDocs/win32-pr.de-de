---
description: Die folgenden Enumerationen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Asynchrone Druck Benachrichtigungs Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362450"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="d30be-103">Asynchrone Druck Benachrichtigungs Enumerationen</span><span class="sxs-lookup"><span data-stu-id="d30be-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="d30be-104">Die folgenden Enumerationen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.</span><span class="sxs-lookup"><span data-stu-id="d30be-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d30be-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d30be-105">In this section</span></span>



| <span data-ttu-id="d30be-106">Enumeration</span><span class="sxs-lookup"><span data-stu-id="d30be-106">Enumeration</span></span>                                                                               | <span data-ttu-id="d30be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d30be-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d30be-108">**Printasyncnotifyconversation-Stil**</span><span class="sxs-lookup"><span data-stu-id="d30be-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="d30be-109">Gibt an, ob die Kommunikation bidirektional oder unidirektional zwischen Anwendungen und Druckspooler-gehosteten Komponenten wie Druckertreibern, Druck Prozessoren und Port Überwachungen ist.</span><span class="sxs-lookup"><span data-stu-id="d30be-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="d30be-110">**Printasyncnotifyerror**</span><span class="sxs-lookup"><span data-stu-id="d30be-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="d30be-111">Gibt den Fehlercode Teil des **HRESULT** an, der nach einem asynchronen Benachrichtigungs Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d30be-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="d30be-112">**Printasyncnotif yuserfilter**</span><span class="sxs-lookup"><span data-stu-id="d30be-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="d30be-113">Gibt an, ob Benachrichtigungen nur an Abhör Anwendungen gesendet werden, die dem gleichen Benutzer wie der vom Druck Spooler gehostete Absender zugeordnet sind, oder zu einem umfassenderen Satz von lauschenden Anwendungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="d30be-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




