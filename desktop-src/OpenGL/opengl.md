---
title: OpenGL
description: Als Softwareschnittstelle für Grafikhardware rendert OpenGL mehrdimensionale Objekte in einen Framebuffer.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474045"
---
# <a name="opengl"></a><span data-ttu-id="d7f79-103">OpenGL</span><span class="sxs-lookup"><span data-stu-id="d7f79-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="d7f79-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="d7f79-104">Purpose</span></span>

<span data-ttu-id="d7f79-105">Als Softwareschnittstelle für Grafikhardware rendert OpenGL mehrdimensionale Objekte in einen Framebuffer.</span><span class="sxs-lookup"><span data-stu-id="d7f79-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="d7f79-106">Bei der Microsoft-Implementierung von OpenGL für das Windows-Betriebssystem handelt es sich um eine branchenübliche Grafiksoftware, mit der Programmierer qualitativ hochwertige, immer noch animierte, dreidimensionale Farbbilder erstellen können.</span><span class="sxs-lookup"><span data-stu-id="d7f79-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="d7f79-107">Die in diesem Abschnitt beschriebene Version von OpenGL ist 1,1.</span><span class="sxs-lookup"><span data-stu-id="d7f79-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="d7f79-108">Informationen zu OpenGL-en, die unter Windows ausgeführt werden, finden Sie unter [Angle for Windows Store](https://github.com/microsoft/angle/wiki).</span><span class="sxs-lookup"><span data-stu-id="d7f79-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d7f79-109">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="d7f79-109">Where applicable</span></span>

<span data-ttu-id="d7f79-110">OpenGL basiert auf der Kompatibilität von Hardware und Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="d7f79-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="d7f79-111">Diese Architektur erleichtert das Portieren von OpenGL-Programmen von einem System zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="d7f79-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="d7f79-112">Obwohl jedes Betriebssystem besondere Anforderungen erfüllt, kann der OpenGL-Code in vielen Programmen unverändert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7f79-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d7f79-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="d7f79-113">Developer audience</span></span>

<span data-ttu-id="d7f79-114">OpenGL ist für die Verwendung durch C/C++-Programmierer konzipiert und erfordert Vertrautheit mit der grafischen Benutzeroberfläche von Windows und der Nachrichten gesteuerten Architektur.</span><span class="sxs-lookup"><span data-stu-id="d7f79-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d7f79-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f79-115">Run-time requirements</span></span>

<span data-ttu-id="d7f79-116">Weitere Informationen dazu, welche Betriebssysteme für eine bestimmte Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="d7f79-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d7f79-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d7f79-117">In this section</span></span>



| <span data-ttu-id="d7f79-118">Thema</span><span class="sxs-lookup"><span data-stu-id="d7f79-118">Topic</span></span>                                             | <span data-ttu-id="d7f79-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7f79-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7f79-120">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d7f79-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="d7f79-121">Allgemeine Informationen zur Funktionsweise von OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d7f79-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="d7f79-122">Verweis</span><span class="sxs-lookup"><span data-stu-id="d7f79-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="d7f79-123">Dokumentation für Funktionen, Strukturen und andere Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="d7f79-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="d7f79-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7f79-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="d7f79-125">Beispiele für OpenGL-Code.</span><span class="sxs-lookup"><span data-stu-id="d7f79-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="d7f79-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7f79-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f79-127">DirectX-Grafiken und -Spiele</span><span class="sxs-lookup"><span data-stu-id="d7f79-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="d7f79-128">[Immer noch Bild](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7f79-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d7f79-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7f79-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d7f79-130">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="d7f79-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="d7f79-131">Windows-Abbild Erfassung</span><span class="sxs-lookup"><span data-stu-id="d7f79-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="d7f79-132">Windows Multimedia</span><span class="sxs-lookup"><span data-stu-id="d7f79-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="d7f79-133">[Windows-API](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7f79-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

