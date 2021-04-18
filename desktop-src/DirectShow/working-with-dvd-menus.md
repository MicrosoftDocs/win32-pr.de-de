---
description: Arbeiten mit DVD-Menüs
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Arbeiten mit DVD-Menüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351177"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="b5589-103">Arbeiten mit DVD-Menüs</span><span class="sxs-lookup"><span data-stu-id="b5589-103">Working With DVD Menus</span></span>

<span data-ttu-id="b5589-104">Der DVD-Navigator kann ein Menü anzeigen, wenn der Benutzer eine Schaltfläche aktiviert, oder wenn der Navigator die erste Wiedergabe Domäne eingibt.</span><span class="sxs-lookup"><span data-stu-id="b5589-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="b5589-105">Um ein Menü Programm gesteuert anzuzeigen, müssen Sie die [**IDvdControl2:: showmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b5589-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="b5589-106">Es gibt mehrere Möglichkeiten, Menü Schaltflächen Programm gesteuert auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="b5589-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="b5589-107">Um eine Schaltfläche nach Nummer auszuwählen, nennen Sie [**IDvdControl2:: selectbutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="b5589-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="b5589-108">Die Schaltflächen sind von 1 bis 36 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="b5589-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="b5589-109">Die [**IDvdInfo2:: getcurrentbutton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) -Methode gibt die Anzahl der verfügbaren Schaltflächen zurück.</span><span class="sxs-lookup"><span data-stu-id="b5589-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="b5589-110">Um eine Schaltfläche in Relation zur Position der aktuell ausgewählten Schaltfläche auszuwählen, nennen Sie [**IDvdControl2:: selectrelativebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="b5589-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="b5589-111">Sie können eine Schaltfläche in der Richtung oben, nach unten, Links oder rechts auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5589-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="b5589-112">Um eine Schaltfläche anhand ihrer Koordinaten innerhalb des Fensters auszuwählen, nennen Sie [**IDvdControl2:: selectatposition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="b5589-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="b5589-113">Diese Methode nimmt (x, y)-Koordinaten in Relation zum Client Bereich des Videofensters.</span><span class="sxs-lookup"><span data-stu-id="b5589-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="b5589-114">(Für den fensterlosen Modus ist dies das Anwendungsfenster.) Wenn an dieser Stelle keine Schaltfläche vorhanden ist, gibt die Methode VFW \_ E \_ DVD \_ No \_ Button zurück.</span><span class="sxs-lookup"><span data-stu-id="b5589-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="b5589-115">Außerdem gibt es mehrere Möglichkeiten, eine Schaltfläche zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="b5589-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="b5589-116">Um eine Schaltfläche nach Zahl zu aktivieren, müssen Sie [**IDvdControl2:: selectandactivatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b5589-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="b5589-117">Um eine Schaltfläche über Ihre Koordinaten zu aktivieren, müssen Sie [**IDvdControl2:: activateatposition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b5589-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="b5589-118">Um die Schaltfläche zu aktivieren, die derzeit ausgewählt ist, aufrufen Sie [**IDvdControl2:: activatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="b5589-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="b5589-119">Wenn keine Schaltfläche ausgewählt ist, gibt die Methode VFW \_ E \_ DVD \_ No \_ Button zurück.</span><span class="sxs-lookup"><span data-stu-id="b5589-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="b5589-120">Beachten Sie, dass durch das Auswählen einer Schaltfläche nur die Rahmen hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="b5589-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="b5589-121">Damit der zugeordnete Befehl ausgelöst wird, muss die Schaltfläche aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b5589-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="b5589-122">Die programmgesteuerte Aktivierung einer Schaltfläche kann auf verschiedene Weise erfolgen, aber die Schaltfläche muss immer ausgewählt werden, bevor Sie aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5589-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5589-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5589-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5589-124">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b5589-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



