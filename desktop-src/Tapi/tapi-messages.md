---
description: Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen. Alle diese Nachrichten werden über den Nachrichten Benachrichtigungs Mechanismus, der von der Anwendung in lineinitializeex angegeben wurde, an die Anwendung gesendet.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: TAPI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368946"
---
# <a name="tapi-messages"></a><span data-ttu-id="51c88-104">TAPI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="51c88-104">TAPI Messages</span></span>

<span data-ttu-id="51c88-105">Nachrichten werden verwendet, um die Anwendung über asynchrone Ereignisse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="51c88-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="51c88-106">Alle diese Nachrichten werden über den Nachrichten Benachrichtigungs Mechanismus, der von der Anwendung in [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)angegeben wurde, an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="51c88-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="51c88-107">Die Meldung enthält immer ein Handle für das relevante Objekt (Telefon, Zeile oder Anruf), das die Anwendung verwenden kann, um den Nachrichtentyp zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="51c88-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="51c88-108">Bestimmte Nachrichten werden verwendet, um die Anwendung über eine Änderung des Status eines Objekts zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="51c88-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="51c88-109">Diese Nachrichten stellen das Objekt Handle bereit und geben Aufschluss darüber, welches Status Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="51c88-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="51c88-110">Die Anwendung kann die entsprechende "Get Status"-Funktion des-Objekts abrufen, um den vollständigen Status des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51c88-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="51c88-111">Wenn ein Ereignis auftritt, können Nachrichten an NULL, eine oder mehrere Anwendungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="51c88-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="51c88-112">Die Zielanwendungen für eine Nachricht werden durch eine Reihe unterschiedlicher Faktoren bestimmt. dazu gehören die Bedeutung der Nachricht, die Berechtigung der Anwendung für das Objekt, ob die Anwendung die Anforderung initiiert hat, für die die Nachricht ein direktes Ergebnis ist, und die Nachrichten Maskierung, die von der Anwendung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="51c88-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="51c88-113">Beachten Sie die folgenden Punkte zu Nachrichten:</span><span class="sxs-lookup"><span data-stu-id="51c88-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="51c88-114">Asynchrone Antwort Nachrichten werden nur an die Anwendung gesendet, von der die Anforderung stammt, und können nicht maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="51c88-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="51c88-115">Nachrichten, die den Abschluss der Ziffern-oder Tongenerierung oder die Erfassung von Ziffern signalisieren, werden nur an die Anwendung gesendet, die die Ziffern-oder Tongenerierung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="51c88-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="51c88-116">Nachrichten, die Zeilen-oder Adress Zustandsänderungen angeben, werden an alle Anwendungen gesendet, die die Zeile geöffnet haben, solange die Nachricht durch [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="51c88-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="51c88-117">Nachrichten, die auf den Ansichts-und den Rückruf von Informationen hinweisen, werden an alle Anwendungen gesendet, die ein Handle für den-Befehl haben</span><span class="sxs-lookup"><span data-stu-id="51c88-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="51c88-118">Nachrichten, die eine Ziffern Erkennung, eine Ton Erkennung oder eine Medientyp Erkennung signalisieren, werden an die Anwendungen gesendet, die die Überwachung dieses Ereignisses angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="51c88-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="51c88-119">Dieser Abschnitt enthält die Referenzinformationen für die folgenden TAPI-Meldungen:</span><span class="sxs-lookup"><span data-stu-id="51c88-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="51c88-120">Unterstützte telefonienachrichten</span><span class="sxs-lookup"><span data-stu-id="51c88-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="51c88-121">Callcentermeldungen</span><span class="sxs-lookup"><span data-stu-id="51c88-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="51c88-122">Formatierte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="51c88-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="51c88-123">Zeilen Geräte Meldungen</span><span class="sxs-lookup"><span data-stu-id="51c88-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="51c88-124">Geräte Nachrichten per Telefon</span><span class="sxs-lookup"><span data-stu-id="51c88-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



