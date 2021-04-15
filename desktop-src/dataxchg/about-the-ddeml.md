---
title: Informationen zur Ddeml
description: In diesem Thema wird der dynamische Datenaustausch erläutert.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows-Benutzeroberfläche, dynamischer Datenaustausch (DDE)
- Dynamischer Datenaustausch (DDE), Informationen zu
- DDE (dynamischer Datenaustausch), Informationen zu
- Datenaustausch, dynamischer Datenaustausch (DDE)
- Windows-Benutzeroberfläche, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
- Dynamischer Datenaustausch Management Library (Ddeml), Informationen zu
- Ddeml (dynamischer Datenaustausch Verwaltungs Bibliothek), Informationen zu
- Datenaustausch, dynamischer Datenaustausch Verwaltungs Bibliothek (Ddeml)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516088"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="c814f-111">Informationen zur Ddeml</span><span class="sxs-lookup"><span data-stu-id="c814f-111">About the DDEML</span></span>

<span data-ttu-id="c814f-112">Dynamischer Datenaustausch (DDE) unterscheidet sich vom Datenübertragungsmechanismus für Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="c814f-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="c814f-113">Ein Unterschied besteht darin, dass die Zwischenablage fast immer als einmalige Antwort auf eine bestimmte Aktion durch den Benutzer verwendet wird – z. b. Wenn Sie in einem Menü auf **Einfügen** klicken.</span><span class="sxs-lookup"><span data-stu-id="c814f-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="c814f-114">Obwohl DDE auch von einem Benutzer initiiert werden kann, wird es in der Regel ohne weitere Beteiligung des Benutzers fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c814f-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="c814f-115">Die dynamischer Datenaustausch Management Library (Ddeml) stellt eine Schnittstelle bereit, die das Hinzufügen von DDE-Funktionen zu einer Anwendung vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c814f-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="c814f-116">Anstatt DDE-Nachrichten direkt zu senden, zu veröffentlichen und zu verarbeiten, verwendet eine Anwendung die von der Ddeml bereitgestellten Funktionen zum Verwalten von DDE-Konversationen.</span><span class="sxs-lookup"><span data-stu-id="c814f-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="c814f-117">Eine DDE-Konversation ist die Interaktion zwischen Client-und Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c814f-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="c814f-118">Die Ddeml bietet auch eine Möglichkeit zum Verwalten der Zeichen folgen und Daten, die von DDE-Anwendungen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="c814f-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="c814f-119">Anstatt Atome und Zeiger auf freigegebene Speicher Objekte zu verwenden, erstellen und verarbeiten DDE-Anwendungen Zeichen folgen Handles, die Zeichen folgen und Daten Handles identifizieren, mit denen DDE-Objekte identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c814f-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="c814f-120">Die Ddeml stellt eine Funktion ([**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) bereit, die es einer Serveranwendung ermöglicht, die von ihr unterstützten Dienstnamen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c814f-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="c814f-121">Die Dienstnamen werden dann an andere Anwendungen im System übertragen, die die Namen zum Herstellen einer Verbindung mit dem Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="c814f-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="c814f-122">Die Ddeml gewährleistet außerdem die Kompatibilität zwischen DDE-Anwendungen, da Sie das DDE-Protokoll konsistent implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c814f-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="c814f-123">Vorhandene Anwendungen, die das Nachrichten basierte DDE-Protokoll verwenden, sind vollständig kompatibel mit denen, die die Ddeml verwenden; Das heißt, eine Anwendung, die Nachrichten basiertes DDE verwendet, kann Konversationen einrichten und Transaktionen mit Anwendungen ausführen, die die Ddeml verwenden.</span><span class="sxs-lookup"><span data-stu-id="c814f-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="c814f-124">Anstatt DDE-Nachrichten in der neuen Anwendung zu verwenden, nutzen Sie die Ddeml und die vielen Verbesserungen, die Sie bietet.</span><span class="sxs-lookup"><span data-stu-id="c814f-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="c814f-125">Um die Ddeml zu verwenden, müssen Sie die Ddeml einschließen. H-Header Datei in ihren Quelldateien, Verknüpfung mit der user32. LIB-Datei, und stellen Sie sicher, dass sich die DDEML.DLL Datei im Systempfad befindet.</span><span class="sxs-lookup"><span data-stu-id="c814f-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="c814f-126">Wenn eine Ddeml-Funktion fehlschlägt, kann eine Anwendung die [**ddegetlasterror**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) -Funktion aufrufen, um die Ursache des Fehlers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c814f-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="c814f-127">**DDE GetLastError** gibt einen Fehlerwert zurück, der die Ursache des letzten Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="c814f-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




