---
description: In diesem Thema wird beschrieben, wie Sie den Status des Druckauftrags für den Benutzer anzeigen und die Option zum Abbrechen eines Druckauftrags, der gerade ausgeführt wird, zur Verfügung stellen.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Vorgehensweise: Anzeigen des Status des Druckauftrags'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358437"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="22ea0-103">Vorgehensweise: Anzeigen des Status des Druckauftrags</span><span class="sxs-lookup"><span data-stu-id="22ea0-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="22ea0-104">In diesem Thema wird beschrieben, wie Sie den Status des Druckauftrags für den Benutzer anzeigen und die Option zum Abbrechen eines Druckauftrags, der gerade ausgeführt wird, zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="22ea0-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="22ea0-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="22ea0-105">Overview</span></span>

<span data-ttu-id="22ea0-106">Ein Dialogfeld zum Drucken des Status führt in der Regel die folgenden Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="22ea0-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="22ea0-107">Zeigt den Status des Druckauftrags für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="22ea0-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="22ea0-108">Starten Sie den druckverarbeitungs Thread.</span><span class="sxs-lookup"><span data-stu-id="22ea0-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="22ea0-109">Zeigen Sie eine Schaltfläche **Abbrechen** an, damit der Benutzer einen Druckauftrag beenden kann, bevor er abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="22ea0-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="22ea0-110">Streng genommen muss die Prozedur zum Drucken des Dialog Felds nur den Druckauftrag für den Benutzer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="22ea0-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="22ea0-111">Da die anderen beiden Funktionen in der vorangehenden Liste jedoch eng miteinander verknüpft sind, sind Sie auch in diesem Modul enthalten.</span><span class="sxs-lookup"><span data-stu-id="22ea0-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="22ea0-112">Anzeigen des Status des Druckauftrags</span><span class="sxs-lookup"><span data-stu-id="22ea0-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="22ea0-113">Im Dialogfeld "Druck Status" werden die folgenden Fenster Meldungen behandelt.</span><span class="sxs-lookup"><span data-stu-id="22ea0-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="22ea0-114">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="22ea0-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="22ea0-115">Initialisiert die Steuerelemente, die im Dialogfeld verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22ea0-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="22ea0-116">**WM- \_ SetCursor**</span><span class="sxs-lookup"><span data-stu-id="22ea0-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="22ea0-117">Legt den Cursor auf einen Zeiger fest, wenn der Benutzer einen Druckauftrag abbrechen kann, und auf den warte Cursor, wenn sich der Druckauftrag an einem Punkt befindet, an dem er nicht abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="22ea0-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="22ea0-118">**Drucken \_ des \_ \_ Druckens des Benutzers**</span><span class="sxs-lookup"><span data-stu-id="22ea0-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="22ea0-119">Legt die Statusanzeige Parameter für den Druckauftrag fest und erstellt den Druck Thread, um mit der Verarbeitung des Druckauftrags zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="22ea0-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="22ea0-120">Dies ist eine anwendungsspezifische Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="22ea0-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="22ea0-121">**WM \_ -Befehl-IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="22ea0-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="22ea0-122">Legt das Ereignis abbrechen fest, um den Druck Verarbeitungs Thread anzuweisen, den Druckauftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="22ea0-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="22ea0-123">**Benutzer \_ Druck \_ Status- \_ Update**</span><span class="sxs-lookup"><span data-stu-id="22ea0-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="22ea0-124">Aktualisiert die Statusanzeige und den Status Text, um den aktuellen Status des Druckauftrags anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22ea0-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="22ea0-125">Dies ist eine anwendungsspezifische Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="22ea0-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="22ea0-126">**Benutzer \_ Druck \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="22ea0-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="22ea0-127">Legt den schließenden Status Text im Dialogfeld "Status" fest, um anzugeben, dass der Druckauftrag geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="22ea0-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="22ea0-128">Dies ist eine anwendungsspezifische Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="22ea0-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="22ea0-129">**Benutzer \_ Druck \_ vollständig**</span><span class="sxs-lookup"><span data-stu-id="22ea0-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="22ea0-130">Zeigt die Meldung "Druckauftrag vollständig" für den Benutzer an und gibt Handles und Ereignisse frei, die in diesem Druckauftrag verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="22ea0-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="22ea0-131">Dies ist eine anwendungsspezifische Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="22ea0-131">This is an application-specific window message.</span></span>

 

 



