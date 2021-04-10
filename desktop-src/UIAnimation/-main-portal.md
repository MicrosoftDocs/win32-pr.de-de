---
title: Windows-Animations-Manager
description: Der Windows Animation Manager (Windows-Animation) ermöglicht eine umfangreiche Animation von Benutzeroberflächen Elementen.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows Animation Windows Animation, Portal
- Windows Animation Manager-Windows-Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948863"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="7ea92-105">Windows-Animations-Manager</span><span class="sxs-lookup"><span data-stu-id="7ea92-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="7ea92-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="7ea92-106">Purpose</span></span>

<span data-ttu-id="7ea92-107">Der Windows Animation Manager (Windows-Animation) ermöglicht eine umfangreiche Animation von Benutzeroberflächen Elementen.</span><span class="sxs-lookup"><span data-stu-id="7ea92-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="7ea92-108">Es wurde entwickelt, um den Prozess des Hinzufügens von Animationen zur Benutzeroberfläche einer Anwendung zu vereinfachen und Entwicklern das Implementieren von Animationen zu ermöglichen, die nahtlos, natürlich und interaktiv sind.</span><span class="sxs-lookup"><span data-stu-id="7ea92-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="7ea92-109">Das Animations Framework verwaltet die Planung und die Ausführung von Animationen.</span><span class="sxs-lookup"><span data-stu-id="7ea92-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="7ea92-110">Es stellt eine Bibliothek nützlicher mathematischer Funktionen zum Angeben des Verhaltens eines Benutzeroberflächen Elements im Zeitverlauf bereit und ermöglicht es Entwicklern außerdem, benutzerdefinierte Funktionen zu implementieren, die zusätzliche Verhaltensweisen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7ea92-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="7ea92-111">Das Rendering wird von der Windows-Animation nicht durchgeführt. Sie kann mit jeder beliebigen Grafik Plattform verwendet werden, einschließlich Direct2D, Direct3D oder GDI+.</span><span class="sxs-lookup"><span data-stu-id="7ea92-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7ea92-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7ea92-112">In this section</span></span>



| <span data-ttu-id="7ea92-113">Thema</span><span class="sxs-lookup"><span data-stu-id="7ea92-113">Topic</span></span>                                                                                   | <span data-ttu-id="7ea92-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ea92-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ea92-115">Entwicklungs Leit Faden für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="7ea92-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="7ea92-116">Im Entwicklerhandbuch finden Sie eine Übersicht über die Windows-Animation und einen Beispielcode, der die grundlegenden Animations Aufgaben behandelt.</span><span class="sxs-lookup"><span data-stu-id="7ea92-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="7ea92-117">Referenz zur Windows-Animation</span><span class="sxs-lookup"><span data-stu-id="7ea92-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="7ea92-118">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für den Windows-Animations-Manager.</span><span class="sxs-lookup"><span data-stu-id="7ea92-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="7ea92-119">Beispiele für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="7ea92-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="7ea92-120">Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7ea92-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="7ea92-121">Glossar für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="7ea92-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="7ea92-122">Dieses Glossar enthält Begriffe und acronyme, die für Entwickler interessant sind, die den Windows-Animations-Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ea92-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="7ea92-123">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="7ea92-123">Developer audience</span></span>

<span data-ttu-id="7ea92-124">Die Windows-Animation ist für die Verwendung durch erfahrene C/C++-Entwickler konzipiert, die mit com, Programmier Konzepten für die Benutzeroberfläche und allgemeinen Animations Konzepten vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="7ea92-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7ea92-125">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="7ea92-125">Run-time requirements</span></span>

<span data-ttu-id="7ea92-126">Der Windows Animation Manager wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7ea92-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="7ea92-127">Anwendungen, die Unterstützung für Windows Animation Manager unter Windows Vista benötigen, können das Platt Form Update für Windows Vista nutzen.</span><span class="sxs-lookup"><span data-stu-id="7ea92-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="7ea92-128">Anwendungen, für die ein Platt Form Update für Windows Vista erforderlich ist, können Windows Update überprüfen, ob es installiert ist, oder Sie können es im Hintergrund herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="7ea92-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="7ea92-129">Weitere Informationen finden Sie unter Informationen zum [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7ea92-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ea92-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ea92-130">Additional resources</span></span>

-   <span data-ttu-id="7ea92-131">[Übersicht über Windows Scenic Animation](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (Video)</span><span class="sxs-lookup"><span data-stu-id="7ea92-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="7ea92-132">[In Windows 7: Deep Dive und Tutorial zu Animation Manager](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (Video)</span><span class="sxs-lookup"><span data-stu-id="7ea92-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="7ea92-133">[Windows-Animation-erweiterte Themen](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (Video)</span><span class="sxs-lookup"><span data-stu-id="7ea92-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="7ea92-134">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="7ea92-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="7ea92-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ea92-135">Related topics</span></span>

[<span data-ttu-id="7ea92-136">Übersicht über Animationen (.NET Framework)</span><span class="sxs-lookup"><span data-stu-id="7ea92-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)