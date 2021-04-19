---
title: Maus Eingaben (beginnen Sie mit Win32 und C++)
description: Mauseingabe
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339107"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="28818-103">Maus Eingaben (beginnen Sie mit Win32 und C++)</span><span class="sxs-lookup"><span data-stu-id="28818-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="28818-104">Windows unterstützt Mäuse mit bis zu fünf Schaltflächen: Links, zentriert und rechts sowie zwei zusätzliche Schaltflächen namens XButton1 und XButton2.</span><span class="sxs-lookup"><span data-stu-id="28818-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![eine Abbildung, in der die Schaltflächen links (1), rechts (2), Mittel (3) und XButton1 (4) angezeigt werden.](images/mouse.png)

<span data-ttu-id="28818-106">Die meisten Mäuse für Windows haben mindestens die linke und die Rechte Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="28818-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="28818-107">Die linke Maustaste wird zum zeigen, auswählen, ziehen usw. verwendet.</span><span class="sxs-lookup"><span data-stu-id="28818-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="28818-108">Mit der rechten Maustaste wird in der Regel ein Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28818-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="28818-109">Einige Mäuse haben ein Mausrad zwischen den linken und rechten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="28818-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="28818-110">Abhängig von der Maus kann das Mausrad auch klickbar sein, sodass es die mittlere Schaltfläche ist.</span><span class="sxs-lookup"><span data-stu-id="28818-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="28818-111">Die Schaltflächen XButton1 und XButton2 befinden sich häufig auf den Seiten der Maus, in der Nähe der Basis.</span><span class="sxs-lookup"><span data-stu-id="28818-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="28818-112">Diese zusätzlichen Schaltflächen sind nicht auf allen Mäusen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28818-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="28818-113">Falls vorhanden, werden die Schaltflächen XButton1 und XButton2 häufig einer Anwendungsfunktion zugeordnet, z. b. vorwärts-und rückwärts Navigation in einem Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="28818-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="28818-114">Links übergebene Benutzer finden es häufig besser, die Funktionen der linken und rechten Schaltflächen auszutauschen – indem Sie die Rechte Schaltfläche als Zeiger und die linke Schaltfläche verwenden, um das Kontextmenü anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="28818-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="28818-115">Aus diesem Grund werden in der Windows-Hilfe Dokumentation die Begriffe *primär Schaltfläche* und *Sekundär Schaltfläche* verwendet, die auf die logische Funktion und nicht auf die physische Platzierung verweisen.</span><span class="sxs-lookup"><span data-stu-id="28818-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="28818-116">In der Standardeinstellung (rechtsseitig übergeben) ist die linke Schaltfläche die primäre Schaltfläche, und die Rechte Taste ist die sekundäre Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="28818-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="28818-117">Die Begriffe mit der *rechten Maustaste klicken* und mit der *linken Maustaste* auf logische Aktionen verweisen.</span><span class="sxs-lookup"><span data-stu-id="28818-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="28818-118">Klicken Sie mit der *rechten Maustaste* auf die Schaltfläche primär, und zwar unabhängig davon, ob sich die Schaltfläche auf der rechten oder linken Seite der Maus befindet.</span><span class="sxs-lookup"><span data-stu-id="28818-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="28818-119">Unabhängig davon, wie der Benutzer die Maus konfiguriert, übersetzt Windows automatisch Maus Meldungen, sodass Sie konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="28818-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="28818-120">Der Benutzer kann die primären und sekundären Schaltflächen in der Mitte der Verwendung des Programms austauschen und wirkt sich nicht darauf aus, wie sich das Programm verhält.</span><span class="sxs-lookup"><span data-stu-id="28818-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="28818-121">Die MSDN-Dokumentation verwendet die Schaltfläche mit den *rechten* und die *linke Schalt* Fläche, um die Schaltfläche *primär* und *Sekundär*</span><span class="sxs-lookup"><span data-stu-id="28818-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="28818-122">Diese Terminologie ist mit den Namen der Fenster Meldungen für Maus Eingaben konsistent.</span><span class="sxs-lookup"><span data-stu-id="28818-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="28818-123">Beachten Sie, dass die physischen linken und rechten Schaltflächen möglicherweise ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="28818-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="28818-124">Nächste</span><span class="sxs-lookup"><span data-stu-id="28818-124">Next</span></span>

[<span data-ttu-id="28818-125">Antworten auf Mausklicks</span><span class="sxs-lookup"><span data-stu-id="28818-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




