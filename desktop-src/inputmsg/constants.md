---
title: Zeiger Eingabe Meldungen und Benachrichtigungs Konstanten
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Zeiger Eingabe Meldungen und Benachrichtigungs Konstanten.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106358190"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="401b4-103">Zeiger Eingabe Meldungen und Benachrichtigungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="401b4-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="401b4-104">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Zeiger Eingabe Meldungen und Benachrichtigungs](messages-and-notifications-portal.md) Konstanten.</span><span class="sxs-lookup"><span data-stu-id="401b4-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="401b4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="401b4-105">In this section</span></span>



| <span data-ttu-id="401b4-106">Thema</span><span class="sxs-lookup"><span data-stu-id="401b4-106">Topic</span></span>                                                                             | <span data-ttu-id="401b4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="401b4-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="401b4-108">**Modifiziererschlüsselzustand**</span><span class="sxs-lookup"><span data-stu-id="401b4-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="401b4-109">Gibt an, welche Tastatur Modifizierertasten beim Generieren der Eingabe gedrückt wurden.</span><span class="sxs-lookup"><span data-stu-id="401b4-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="401b4-110">**Pen-Flags**</span><span class="sxs-lookup"><span data-stu-id="401b4-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="401b4-111">Werte, die im Feld " **kflags** " der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="401b4-112">**Stift Maske**</span><span class="sxs-lookup"><span data-stu-id="401b4-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="401b4-113">Werte, die im Feld " **Straf Maske** " der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="401b4-114">**Zeiger Geräte Änderung**</span><span class="sxs-lookup"><span data-stu-id="401b4-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="401b4-115">Werte, die im *wParam* -Parameter der [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) Nachricht übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="401b4-116">**Zeigerflags**</span><span class="sxs-lookup"><span data-stu-id="401b4-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="401b4-117">Werte, die im Feld **pointerflags** der [**POINTER_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="401b4-118">**Zeigernachrichtenflags**</span><span class="sxs-lookup"><span data-stu-id="401b4-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="401b4-119">Werte, die in verschiedenen Zeiger Makros verwendet werden (siehe [Makros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="401b4-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="401b4-120">**Berührungs Flags**</span><span class="sxs-lookup"><span data-stu-id="401b4-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="401b4-121">Werte, die im Feld **touchflags** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="401b4-122">**Berührungs Treffer-Test Fenster**</span><span class="sxs-lookup"><span data-stu-id="401b4-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="401b4-123">Gibt an, wie Nachrichten für Touch-Treffer Tests von Fenstern verarbeitet werden, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="401b4-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="401b4-124">**Berührungs Maske**</span><span class="sxs-lookup"><span data-stu-id="401b4-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="401b4-125">Werte, die im Feld **touchmask** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="401b4-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="401b4-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="401b4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401b4-127">Verweis auf Zeiger-Eingabe Nachricht</span><span class="sxs-lookup"><span data-stu-id="401b4-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

