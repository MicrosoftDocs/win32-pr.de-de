---
title: Verwenden von com in Ihrer Windows-App
description: In Modul 1 dieser Reihe wurde gezeigt, wie ein Fenster erstellt und auf Fenster Meldungen wie WM \_ Paint und WM close reagiert wird \_ . In Modul 2 wird der Component Object Model (com) eingeführt.
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726952"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="1242f-104">Modul 2.</span><span class="sxs-lookup"><span data-stu-id="1242f-104">Module 2.</span></span> <span data-ttu-id="1242f-105">Verwenden von com in Ihrem Windows-Based Programm</span><span class="sxs-lookup"><span data-stu-id="1242f-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="1242f-106">In [Modul 1](your-first-windows-program.md) dieser Reihe wurde gezeigt, wie ein Fenster erstellt und auf Fenster Meldungen wie [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) und [**WM \_ Close**](/windows/desktop/winmsg/wm-close)reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="1242f-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="1242f-107">In Modul 2 wird der Component Object Model (com) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1242f-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="1242f-108">COM ist eine Spezifikation zum Erstellen wiederverwendbarer Softwarekomponenten.</span><span class="sxs-lookup"><span data-stu-id="1242f-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="1242f-109">Viele der Features, die Sie in einem modernen Windows-basierten Programm verwenden werden, basieren auf com, wie z. b. folgendem:</span><span class="sxs-lookup"><span data-stu-id="1242f-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="1242f-110">Grafiken (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="1242f-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="1242f-111">Text (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="1242f-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="1242f-112">Die Windows-Shell</span><span class="sxs-lookup"><span data-stu-id="1242f-112">The Windows Shell</span></span>
-   <span data-ttu-id="1242f-113">Menüband-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1242f-113">The Ribbon control</span></span>
-   <span data-ttu-id="1242f-114">UI-Animation</span><span class="sxs-lookup"><span data-stu-id="1242f-114">UI animation</span></span>

<span data-ttu-id="1242f-115">(Einige Technologien in dieser Liste verwenden eine Teilmenge von com und sind daher nicht "Pure" com.)</span><span class="sxs-lookup"><span data-stu-id="1242f-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="1242f-116">COM hat den Ruf, schwer zu erlernen.</span><span class="sxs-lookup"><span data-stu-id="1242f-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="1242f-117">Und es ist richtig, dass das Schreiben eines neuen Software Moduls zur Unterstützung von com schwierig sein kann.</span><span class="sxs-lookup"><span data-stu-id="1242f-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="1242f-118">Wenn Ihr Programm jedoch nur ein com- *Consumer* ist, kann es sein, dass com leichter zu verstehen ist als erwartet.</span><span class="sxs-lookup"><span data-stu-id="1242f-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="1242f-119">Dieses Modul zeigt, wie COM-basierte APIs in Ihrem Programm aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1242f-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="1242f-120">Außerdem werden einige der Argumente hinter dem Design von com beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1242f-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="1242f-121">Wenn Sie verstehen, warum com genauso konzipiert ist, können Sie mit dem com-Programm effektiver programmieren.</span><span class="sxs-lookup"><span data-stu-id="1242f-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="1242f-122">Der zweite Teil des Moduls beschreibt einige empfohlene Programmiermethoden für com.</span><span class="sxs-lookup"><span data-stu-id="1242f-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="1242f-123">COM wurde in 1993 eingeführt, um das Verknüpfen und Einbetten von Objekten (OLE) 2,0 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1242f-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="1242f-124">Manchmal ist es wichtig, dass com und OLE identisch sind.</span><span class="sxs-lookup"><span data-stu-id="1242f-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="1242f-125">Dies kann ein weiterer Grund dafür sein, dass com schwer zu erlernen ist.</span><span class="sxs-lookup"><span data-stu-id="1242f-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="1242f-126">OLE 2,0 basiert auf com, aber Sie müssen OLE nicht kennen, um com zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="1242f-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="1242f-127">COM ist ein *binärer Standard* und kein Sprachstandard: er definiert die binäre Schnittstelle zwischen einer Anwendung und einer Softwarekomponente.</span><span class="sxs-lookup"><span data-stu-id="1242f-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="1242f-128">Als binärer Standard ist com sprachneutral, obwohl es sich auf natürliche Weise bestimmten C++-Konstrukten zuordnet.</span><span class="sxs-lookup"><span data-stu-id="1242f-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="1242f-129">Dieses Modul konzentriert sich auf drei Hauptziele von com:</span><span class="sxs-lookup"><span data-stu-id="1242f-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="1242f-130">Trennen der Implementierung eines Objekts von der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1242f-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="1242f-131">Verwalten der Lebensdauer eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="1242f-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="1242f-132">Ermitteln der Funktionen eines Objekts zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="1242f-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1242f-133">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1242f-133">In this section</span></span>

-   [<span data-ttu-id="1242f-134">Was ist eine COM-Schnittstelle?</span><span class="sxs-lookup"><span data-stu-id="1242f-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="1242f-135">Initialisieren der com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1242f-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="1242f-136">Fehler Codes in com</span><span class="sxs-lookup"><span data-stu-id="1242f-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="1242f-137">Erstellen eines Objekts in com</span><span class="sxs-lookup"><span data-stu-id="1242f-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="1242f-138">Beispiel: das Dialog Feld "Öffnen"</span><span class="sxs-lookup"><span data-stu-id="1242f-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="1242f-139">Verwalten der Lebensdauer eines Objekts</span><span class="sxs-lookup"><span data-stu-id="1242f-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="1242f-140">Anfordern eines Objekts für eine Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1242f-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="1242f-141">Speicher Belegung in com</span><span class="sxs-lookup"><span data-stu-id="1242f-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="1242f-142">COM-Codierungs Methoden</span><span class="sxs-lookup"><span data-stu-id="1242f-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="1242f-143">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="1242f-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="1242f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1242f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1242f-145">Erlernen Sie das Program mieren für Windows in C++</span><span class="sxs-lookup"><span data-stu-id="1242f-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 