---
title: Makros
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Zeiger Eingabe Meldungen und Benachrichtigungs Makros zum Abrufen von Informationen aus Zeiger Eingabe-Nachrichten Parametern.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "104389753"
---
# <a name="macros"></a><span data-ttu-id="d9e54-103">Makros</span><span class="sxs-lookup"><span data-stu-id="d9e54-103">Macros</span></span>

<span data-ttu-id="d9e54-104">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Zeiger Eingabe Meldungen und Benachrichtigungs](messages-and-notifications-portal.md) Makros zum Abrufen von Informationen aus Zeiger Eingabe-Nachrichten Parametern.</span><span class="sxs-lookup"><span data-stu-id="d9e54-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9e54-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d9e54-105">In this section</span></span>



| <span data-ttu-id="d9e54-106">Thema</span><span class="sxs-lookup"><span data-stu-id="d9e54-106">Topic</span></span>                                                                                  | <span data-ttu-id="d9e54-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9e54-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9e54-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="d9e54-109">Ruft die Zeiger-ID unter Verwendung des angegebenen-Werts ab.</span><span class="sxs-lookup"><span data-stu-id="d9e54-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="d9e54-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="d9e54-111">Überprüft, ob die angegebene Zeiger Nachricht als absichtlich und nicht als versehentlich erachtet wird.</span><span class="sxs-lookup"><span data-stu-id="d9e54-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="d9e54-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="d9e54-113">Überprüft, ob die angegebene Zeiger Eingabe abrupt beendet wurde oder ungültig war, was darauf hinweist, dass die Interaktion nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9e54-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="d9e54-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="d9e54-115">Überprüft, ob der angegebene Zeiger eine fünfte Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9e54-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="d9e54-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="d9e54-117">Überprüft, ob der angegebene Zeiger zuerst eine Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9e54-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="d9e54-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="d9e54-119">Überprüft, ob ein Zeiger Makro das angegebene Flag festlegt.</span><span class="sxs-lookup"><span data-stu-id="d9e54-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="d9e54-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="d9e54-121">Überprüft, ob der angegebene Zeiger die vierte Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9e54-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="d9e54-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="d9e54-123">Überprüft, ob der angegebene Zeiger in Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="d9e54-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="d9e54-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="d9e54-125">Überprüft, ob sich der angegebene Zeiger im Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="d9e54-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="d9e54-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="d9e54-127">Überprüft, ob der angegebene Zeiger ein neuer Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="d9e54-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="d9e54-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="d9e54-129">Überprüft, ob der angegebene Zeiger der primäre Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="d9e54-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="d9e54-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="d9e54-131">Überprüft, ob der angegebene Zeiger eine zweite Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9e54-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="d9e54-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="d9e54-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="d9e54-133">Überprüft, ob der angegebene Zeiger eine dritte Aktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="d9e54-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="d9e54-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9e54-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e54-135">Verweis auf Zeiger-Eingabe Nachricht</span><span class="sxs-lookup"><span data-stu-id="d9e54-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





