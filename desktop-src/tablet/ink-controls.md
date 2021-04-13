---
description: Übersicht über frei Hand Steuerelemente für den Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Ink-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525967"
---
# <a name="ink-controls"></a><span data-ttu-id="1aeb6-103">Ink-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="1aeb6-103">Ink Controls</span></span>

<span data-ttu-id="1aeb6-104">Die Tablet PC-Plattform bietet zwei Steuerelemente: [InkEdit](inkedit-control.md) und [InkPicture](inkpicture-control.md), mit denen Sie Tablet PC-Anwendungen problemlos Handschrift und Handschrifterkennung hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="1aeb6-105">Das InkEdit-Steuerelement verfügt über [verwaltete](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) -und Win32-Versionen, während InkPicture nur über die verwalteten [InkPicture](/previous-versions/ms583740(v=vs.100)) -und [ActiveX](inkpicture-control-reference.md) -Versionen verfügt.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="1aeb6-106">Der Hauptunterschied zwischen den Steuerelementen besteht darin, wie Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="1aeb6-107">Das [InkEdit](inkedit-control.md) -Steuerelement speichert Frei Hand Eingaben standardmäßig als Text, während [InkPicture](inkpicture-control.md) Freihand als frei Hand Daten speichert.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="1aeb6-108">Das [InkEdit](inkedit-control.md) -Steuerelement ist für die Texteingabe durch Handschrifterkennung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="1aeb6-109">[InkPicture](inkpicture-control.md) ist für die Anmerkung gedacht (z. b. das Markieren einer Präsentations Folie oder eines anderen Bilds).</span><span class="sxs-lookup"><span data-stu-id="1aeb6-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="1aeb6-110">Erstellen Sie in verwaltetem Code frei Hand Steuerelemente im gleichen Thread wie der Haupt Thread für das Formular.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="1aeb6-111">Wenn ein [InkEdit](inkedit-control.md) -oder [InkPicture](inkpicture-control.md) -Steuerelement in einem anderen Thread erstellt wird, reagiert die Anwendung möglicherweise nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="1aeb6-112">Sie sollten das Threading Modell explizit in ein Single Thread-Apartment (STA) ändern, bevor Sie ein Ink-Steuerelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="1aeb6-113">Dies bewirkt, dass das Steuerelement im Haupt Thread erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="1aeb6-114">Sie können den folgenden verwalteten C++-Code verwenden, um das Threading Modell explizit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="1aeb6-115">Sie können den folgenden Code verwenden, um in C dasselbe zu tun \# .</span><span class="sxs-lookup"><span data-stu-id="1aeb6-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="1aeb6-116">Um einen Speicher Verluste zu vermeiden, müssen Sie in verwaltetem Code die verwerfen [-Methode explizit](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) für jedes Tablet PC-Steuerelement, an das ein Ereignishandler angefügt wurde, aufgerufen werden, bevor das Steuerelement den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="1aeb6-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="1aeb6-117">In den folgenden Abschnitten werden Freihand Steuerelemente und die Verwendung von frei Hand Steuerelementen in-Anwendungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1aeb6-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="1aeb6-118">Hinzufügen von Ink-Steuerelementen zu einem Projekt</span><span class="sxs-lookup"><span data-stu-id="1aeb6-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="1aeb6-119">InkEdit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1aeb6-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="1aeb6-120">InkPicture-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1aeb6-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 
