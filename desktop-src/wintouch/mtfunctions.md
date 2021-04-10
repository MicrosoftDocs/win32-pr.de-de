---
title: Funktionen (Windows-Eingabe Eingabe)
description: Dieser Abschnitt enthält Funktionen für die Eingabe von Windows-Eingaben.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows-Fingereingabe, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040018"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="06d90-104">Funktionen (Windows-Eingabe Eingabe)</span><span class="sxs-lookup"><span data-stu-id="06d90-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="06d90-105">Dieser Abschnitt enthält Funktionen für die Eingabe von Windows-Eingaben.</span><span class="sxs-lookup"><span data-stu-id="06d90-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="06d90-106">Die folgenden Funktionen werden für die Eingabe von Windows-Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="06d90-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="06d90-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="06d90-107">Function</span></span>                                                                                               | <span data-ttu-id="06d90-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06d90-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06d90-109">**Closetouchinputhandle**</span><span class="sxs-lookup"><span data-stu-id="06d90-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="06d90-110">Schließt ein Fingereingabe handle, gibt ihm zugeordneten Prozess Speicher frei und erklärt das Handle für ungültig.</span><span class="sxs-lookup"><span data-stu-id="06d90-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="06d90-111">**GetTouchInputInfo**</span><span class="sxs-lookup"><span data-stu-id="06d90-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="06d90-112">Ruft ausführliche Informationen zu Finger Eingaben ab, die einem bestimmten Fingereingabe Handle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="06d90-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="06d90-113">**Istouchwindow**</span><span class="sxs-lookup"><span data-stu-id="06d90-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="06d90-114">Überprüft, ob ein angegebenes Fenster Berührungs fähig ist, und ruft optional die Modifiziererflags ab, die für die Berührungs Funktion des Fensters festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="06d90-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="06d90-115">**RegisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="06d90-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="06d90-116">Registriert ein Fenster als Berührungs fähig.</span><span class="sxs-lookup"><span data-stu-id="06d90-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="06d90-117">**Unregistertouchwindow**</span><span class="sxs-lookup"><span data-stu-id="06d90-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="06d90-118">Registriert ein Fenster als nicht mehr als Berührungs fähig.</span><span class="sxs-lookup"><span data-stu-id="06d90-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="06d90-119">SendMessage, PostMessage und verwandte Funktionen</span><span class="sxs-lookup"><span data-stu-id="06d90-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="06d90-120">Enthält Überlegungen zum Weiterleiten von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="06d90-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="06d90-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06d90-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06d90-122">Windows-Eingabe Eingabe</span><span class="sxs-lookup"><span data-stu-id="06d90-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="06d90-123">Leitfaden zur Eingabe der Windows-Eingabe Eingabe</span><span class="sxs-lookup"><span data-stu-id="06d90-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 




