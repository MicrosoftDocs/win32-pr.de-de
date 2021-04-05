---
title: Verwenden von TrackBar-Steuerelementen
description: Dieser Abschnitt enthält Implementierungsdetails und Beispiele für TrackBar-Steuerelemente.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710020"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="da50c-103">Verwenden von TrackBar-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="da50c-103">Using Trackbar Controls</span></span>

<span data-ttu-id="da50c-104">Dieser Abschnitt enthält Implementierungsdetails und Beispiele für TrackBar-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="da50c-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="da50c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="da50c-105">In this section</span></span>



| <span data-ttu-id="da50c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="da50c-106">Topic</span></span>                                                                                                  | <span data-ttu-id="da50c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da50c-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da50c-108">Erstellen einer TrackBar</span><span class="sxs-lookup"><span data-stu-id="da50c-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="da50c-109">Wenn die TrackBar erstellt wird, werden sowohl der Bereich als auch der zugehörige Auswahlbereich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="da50c-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="da50c-110">Die Seitengröße wird auch zu diesem Zeitpunkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da50c-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="da50c-111">Verarbeiten von TrackBar-Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="da50c-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="da50c-112">Trackbars Benachrichtigen das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="da50c-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="da50c-113">Begrenzen der Schieberegler-Bewegung</span><span class="sxs-lookup"><span data-stu-id="da50c-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="da50c-114">Wie in [Informationen zu TrackBar](trackbar-controls.md)-Steuerelementen beschrieben, ist es möglich, einen Teil des TrackBar-Bereichs als Auswahlbereich festzulegen.</span><span class="sxs-lookup"><span data-stu-id="da50c-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="da50c-115">Ein Zweck eines Auswahl Bereichs ist möglicherweise, die Verschiebung des Schiebereglers einzuschränken, sodass einige Teile des vollständigen Bereichs deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="da50c-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="da50c-116">Verwenden von Buddy-Fenstern</span><span class="sxs-lookup"><span data-stu-id="da50c-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="da50c-117">Wenn Sie andere Steuerelemente als Buddy-Fenster für eine TrackBar festlegen, können Sie diese Steuerelemente an den Enden der TrackBar als Bezeichnungen automatisch positionieren.</span><span class="sxs-lookup"><span data-stu-id="da50c-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





