---
description: Ein externer Benutzeroberflächen Handler kann eine beliebige Anzahl von Werten zurückgeben Windows Installer, die in Abhängigkeit von dem im Message Type-Parameter angegebenen schaltentyp (User Interface, UI) an den Handler übergeben werden.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Zurückgeben von Werten von einem externen Benutzeroberflächen Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754201"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="89639-103">Zurückgeben von Werten von einem externen Benutzeroberflächen Handler</span><span class="sxs-lookup"><span data-stu-id="89639-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="89639-104">Ein externer Benutzeroberflächen Handler kann eine beliebige Anzahl von Werten zurückgeben Windows Installer, die in Abhängigkeit von dem im Message Type-Parameter angegebenen schaltentyp (User Interface, UI) an den Handler übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="89639-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="89639-105">Der externe UI-Handler kann die Werte – 1 und 0 jederzeit zurückgeben, da diese nicht mit den Schaltflächen Typen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="89639-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="89639-106">Der Rückgabewert – 1 gibt an, dass im externen UI-Handler ein interner Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="89639-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="89639-107">Der Rückgabewert 0 gibt an, dass der externe UI-Handler die installernachricht nicht verarbeitet hat, und der Installer muss stattdessen die Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="89639-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="89639-108">Bei Nachrichten, die keinen Schalt Flächentyp enthalten, wie z. b. installmessage \_ aktiondata und installmessage \_ Progress, wird die Installation durch die Rückgabe von IDCANCEL abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="89639-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="89639-109">Beim Zurückgeben von IDOK wird das Installationsprogramm benachrichtigt, dass die Nachricht vom externen UI-Handler behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="89639-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="89639-110">Die übrigen Rückgabewerte, wie unten beschrieben, sind direkt mit den Schaltflächen Typen verknüpft, die im Nachrichtentyp enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="89639-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="89639-111">Rückgabewert der externen Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="89639-111">External UI return value</span></span> | <span data-ttu-id="89639-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="89639-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89639-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="89639-113">IDOK</span></span>                     | <span data-ttu-id="89639-114">Der Benutzer hat die Schaltfläche **OK** gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="89639-115">Die Nachrichten Informationen wurden verstanden.</span><span class="sxs-lookup"><span data-stu-id="89639-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="89639-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="89639-116">IDCANCEL</span></span>                 | <span data-ttu-id="89639-117">Die Schaltfläche **Abbrechen** wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="89639-118">Brechen Sie die Installation ab.</span><span class="sxs-lookup"><span data-stu-id="89639-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="89639-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="89639-119">IDABORT</span></span>                  | <span data-ttu-id="89639-120">Die Schaltfläche **Abbrechen** wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="89639-121">Brechen Sie die Installation ab.</span><span class="sxs-lookup"><span data-stu-id="89639-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="89639-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="89639-122">IDRETRY</span></span>                  | <span data-ttu-id="89639-123">Die **Wiederholungs** Schaltfläche wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="89639-124">Wiederholen Sie die Aktion.</span><span class="sxs-lookup"><span data-stu-id="89639-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="89639-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="89639-125">IDIGNORE</span></span>                 | <span data-ttu-id="89639-126">Die **ignorieren** -Schaltfläche wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="89639-127">Ignorieren Sie den Fehler, und fahren Sie fort.</span><span class="sxs-lookup"><span data-stu-id="89639-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="89639-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="89639-128">IDYES</span></span>                    | <span data-ttu-id="89639-129">Die **Ja** -Schaltfläche wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-129">The **YES** button was pressed.</span></span> <span data-ttu-id="89639-130">Die positive Antwort ist mit der aktuellen Ereignis Sequenz fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="89639-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="89639-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="89639-131">IDNO</span></span>                     | <span data-ttu-id="89639-132">Die Schaltfläche **Nein** wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="89639-132">The **NO** button was pressed.</span></span> <span data-ttu-id="89639-133">Die negative Antwort wird nicht mit der aktuellen Abfolge von Ereignissen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="89639-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="89639-134">Wenn z. b. der externe UI-Handler eine Meldung mit dem Format "MB \_ AbortRetryIgnore Message Box Styles" sendet, kann der externe UI-Handler einen der folgenden Werte zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="89639-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="89639-135">– 1 (Fehler im externen UI-Handler)</span><span class="sxs-lookup"><span data-stu-id="89639-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="89639-136">0 (keine Aktion im externen UI-Handler ausgeführt, Windows Installer behandeln)</span><span class="sxs-lookup"><span data-stu-id="89639-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="89639-137">Idabort (Schaltfläche **Abbrechen** )</span><span class="sxs-lookup"><span data-stu-id="89639-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="89639-138">Idretry (Schaltfläche "**wiederholen** " gedrückt)</span><span class="sxs-lookup"><span data-stu-id="89639-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="89639-139">IDIGNORE (Schaltfläche "**ignorieren** " gedrückt)</span><span class="sxs-lookup"><span data-stu-id="89639-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



