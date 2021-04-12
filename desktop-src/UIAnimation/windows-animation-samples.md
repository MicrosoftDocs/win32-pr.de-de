---
title: Beispiele für Windows-Animationen
description: Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animation Windows Animation Windows Animation, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310863"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="2444f-104">Beispiele für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="2444f-104">Windows Animation Samples</span></span>

<span data-ttu-id="2444f-105">Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2444f-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2444f-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2444f-106">In this section</span></span>



| <span data-ttu-id="2444f-107">Thema</span><span class="sxs-lookup"><span data-stu-id="2444f-107">Topic</span></span>                                                                                     | <span data-ttu-id="2444f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2444f-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2444f-109">Beispiel für eine Anwendungs gesteuerte Animation</span><span class="sxs-lookup"><span data-stu-id="2444f-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="2444f-110">Beispiel für eine Zeit Geber gesteuerte Animation</span><span class="sxs-lookup"><span data-stu-id="2444f-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="2444f-111">Beispiel für benutzerdefiniertes Interpolator</span><span class="sxs-lookup"><span data-stu-id="2444f-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="2444f-112">Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2444f-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="2444f-113">Raster Layout-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2444f-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="2444f-114">Veranschaulicht die Verwendung der Windows-Animation mit Direct2D zum Animieren eines Bild Blatts.</span><span class="sxs-lookup"><span data-stu-id="2444f-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="2444f-115">Beispiel für Prioritäts Vergleich</span><span class="sxs-lookup"><span data-stu-id="2444f-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="2444f-116">Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2444f-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="2444f-117">Beispieldateien</span><span class="sxs-lookup"><span data-stu-id="2444f-117">Sample Files</span></span>

<span data-ttu-id="2444f-118">Jedes Beispiel enthält viele der folgenden Schlüsseldateien:</span><span class="sxs-lookup"><span data-stu-id="2444f-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="2444f-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="2444f-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="2444f-120">Definiert den Einstiegspunkt der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2444f-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="2444f-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="2444f-122">Deklariert die CMainWindow-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2444f-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="2444f-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="2444f-124">Initialisiert die Animations Komponenten und die Grafik Plattform, lädt Bilder und rendert den Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="2444f-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>Layoutmanager. h</span><span class="sxs-lookup"><span data-stu-id="2444f-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="2444f-126">Deklariert die clayoutmanager-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2444f-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>Layoutmanager. cpp</span><span class="sxs-lookup"><span data-stu-id="2444f-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="2444f-128">Berechnet das Layout von Bildern im Hauptfenster, erstellt Storyboards, fügt dem Storyboard Übergänge hinzu und plant das Storyboard.</span><span class="sxs-lookup"><span data-stu-id="2444f-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Miniaturansicht. h</span><span class="sxs-lookup"><span data-stu-id="2444f-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="2444f-130">Deklariert die cminiatur-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2444f-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="2444f-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Miniaturansicht. cpp</span><span class="sxs-lookup"><span data-stu-id="2444f-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="2444f-132">Erstellt Animations Variablen und rendert Miniaturansichten.</span><span class="sxs-lookup"><span data-stu-id="2444f-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2444f-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2444f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2444f-134">Entwicklungs Leit Faden für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="2444f-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="2444f-135">Referenz zur Windows-Animation</span><span class="sxs-lookup"><span data-stu-id="2444f-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





