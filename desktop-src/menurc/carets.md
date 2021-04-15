---
title: Caretzeichen
description: In diesem Abschnitt werden die Caretzeichen erläutert, die Zeilen, Blöcke oder Bitmaps im Client Bereich eines Fensters blinken.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- Ressourcen, Caretzeichen
- Caretzeichen, Info
- blinkende Linien
- blinkende Blöcke
- blinken von Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104393826"
---
# <a name="carets"></a><span data-ttu-id="2b5be-108">Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="2b5be-108">Carets</span></span>

<span data-ttu-id="2b5be-109">Ein *Caretzeichen* ist eine blinkende Zeile, ein Block oder eine Bitmap im Client Bereich eines Fensters.</span><span class="sxs-lookup"><span data-stu-id="2b5be-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="2b5be-110">Die Einfügemarke gibt in der Regel den Ort an, an dem Text oder Grafiken eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2b5be-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="2b5be-111">In der folgenden Abbildung werden einige allgemeine Variationen der Darstellung der Einfügemarke veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2b5be-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Zeigt fünf unterschiedliche Möglichkeiten, wie ein Caretzeichen angezeigt werden kann.](images/cscrt-01.png)

<span data-ttu-id="2b5be-113">Anwendungen können eine Einfügemarke erstellen, die Blinkzeit ändern und die Einfügemarke anzeigen, ausblenden oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="2b5be-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="2b5be-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2b5be-114">In This Section</span></span>



| <span data-ttu-id="2b5be-115">Name</span><span class="sxs-lookup"><span data-stu-id="2b5be-115">Name</span></span>                                   | <span data-ttu-id="2b5be-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b5be-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2b5be-117">Informationen zu Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="2b5be-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="2b5be-118">Erläutert Caretzeichen.</span><span class="sxs-lookup"><span data-stu-id="2b5be-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="2b5be-119">Verwenden von Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="2b5be-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="2b5be-120">Code Beispiele, die das Ausführen von Aufgaben im Zusammenhang mit Caretzeichen veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="2b5be-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="2b5be-121">Verweis auf Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="2b5be-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="2b5be-122">Enthält die API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="2b5be-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="2b5be-123">Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="2b5be-123">Caret Functions</span></span>



| <span data-ttu-id="2b5be-124">Name</span><span class="sxs-lookup"><span data-stu-id="2b5be-124">Name</span></span>                                           | <span data-ttu-id="2b5be-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b5be-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b5be-126">**Auflistungs Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="2b5be-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="2b5be-127">Erstellt eine neue Form für die System Einfügemarke und weist dem angegebenen Fenster den Besitz der Einfügemarke zu.</span><span class="sxs-lookup"><span data-stu-id="2b5be-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="2b5be-128">Die Form des Caretzeichen kann eine Linie, ein Block oder eine Bitmap sein.</span><span class="sxs-lookup"><span data-stu-id="2b5be-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="2b5be-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="2b5be-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="2b5be-130">Zerstört die aktuelle Form des Caretzeichen, gibt die Einfügemarke aus dem Fenster frei und entfernt die Einfügemarke aus dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="2b5be-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="2b5be-131">**Getcaretblinktime**</span><span class="sxs-lookup"><span data-stu-id="2b5be-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="2b5be-132">Ruft die Zeit ab, die zum Umkehren der Pixel der Einfügemarke benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2b5be-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="2b5be-133">Der Benutzer kann diesen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="2b5be-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="2b5be-134">**Getcaretpos**</span><span class="sxs-lookup"><span data-stu-id="2b5be-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="2b5be-135">Kopiert die Position der Einfügemarke in die angegebene [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="2b5be-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="2b5be-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="2b5be-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="2b5be-137">Entfernt die Einfügemarke aus dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="2b5be-137">Removes the caret from the screen.</span></span> <span data-ttu-id="2b5be-138">Beim Ausblenden einer Einfügemarke wird die aktuelle Form nicht zerstört, oder die Einfügemarke wird ungültig.</span><span class="sxs-lookup"><span data-stu-id="2b5be-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="2b5be-139">**Setcaretblinktime**</span><span class="sxs-lookup"><span data-stu-id="2b5be-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="2b5be-140">Legt die Blinkzeit des Caretzeichen auf die angegebene Anzahl von Millisekunden fest.</span><span class="sxs-lookup"><span data-stu-id="2b5be-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="2b5be-141">Die Blink Zeit ist die verstrichene Zeit (in Millisekunden), die erforderlich ist, um die Pixel des Caretzeichen umzukehren.</span><span class="sxs-lookup"><span data-stu-id="2b5be-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="2b5be-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="2b5be-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="2b5be-143">Verschiebt die Einfügemarke zu den angegebenen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="2b5be-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="2b5be-144">Wenn das Fenster, das die Einfügemarke besitzt, mit dem **CS- \_ owndc** -Klassen Stil erstellt wurde, unterliegen die angegebenen Koordinaten dem Kartenmodus des Geräte Kontexts, der diesem Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b5be-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="2b5be-145">**ShowCaret**</span><span class="sxs-lookup"><span data-stu-id="2b5be-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="2b5be-146">Macht das Caretzeichen auf dem Bildschirm an der aktuellen Position des Caretzeichen sichtbar.</span><span class="sxs-lookup"><span data-stu-id="2b5be-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="2b5be-147">Wenn das Caretzeichen sichtbar wird, beginnt es automatisch mit dem blinken.</span><span class="sxs-lookup"><span data-stu-id="2b5be-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

