---
description: Windows GDI+ ist eine klassenbasierte API für C/C++-Programmierer.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129068"
---
# <a name="gdi"></a><span data-ttu-id="23b06-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="23b06-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="23b06-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="23b06-104">Purpose</span></span>

<span data-ttu-id="23b06-105">Windows GDI+ ist eine klassenbasierte API für C/C++-Programmierer.</span><span class="sxs-lookup"><span data-stu-id="23b06-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="23b06-106">Sie ermöglicht es Anwendungen, Grafiken und formatierten Text sowohl auf der Videoanzeige als auch auf dem Drucker zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23b06-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="23b06-107">Anwendungen, die auf der Microsoft Win32-API basieren, greifen nicht direkt auf die Grafikhardware zu.</span><span class="sxs-lookup"><span data-stu-id="23b06-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="23b06-108">Stattdessen interagiert GDI+ im Auftrag von Anwendungen mit Gerätetreibern.</span><span class="sxs-lookup"><span data-stu-id="23b06-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="23b06-109">GDI+ wird auch von Microsoft Win64 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23b06-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="23b06-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="23b06-110">Where applicable</span></span>

<span data-ttu-id="23b06-111">GDI+-Funktionen und-Klassen werden nicht für die Verwendung in einem Windows-Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23b06-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="23b06-112">Der Versuch, diese Funktionen und Klassen von einem Windows-Dienst zu verwenden, kann zu unerwarteten Problemen führen, wie z. b. verminderter Dienstleistung und Lauf Zeit Ausnahmen oder-Fehler.</span><span class="sxs-lookup"><span data-stu-id="23b06-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="23b06-113">Wenn Sie die GDI+-API verwenden, dürfen Sie niemals zulassen, dass Ihre Anwendung beliebige Schriftarten aus nicht vertrauenswürdigen Quellen herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="23b06-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="23b06-114">Das Betriebssystem erfordert erhöhte Berechtigungen, um sicherzustellen, dass alle installierten Schriftarten vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="23b06-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="23b06-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="23b06-115">Developer audience</span></span>

<span data-ttu-id="23b06-116">Die klassenbasierte GDI+ C++-Schnittstelle ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="23b06-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="23b06-117">Kenntnisse über die grafische Benutzeroberfläche von Windows und die Nachrichten gesteuerte Architektur sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23b06-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="23b06-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="23b06-118">Run-time requirements</span></span>

<span data-ttu-id="23b06-119">GDI+ kann in allen Windows-basierten Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23b06-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="23b06-120">GDI+ wurde in Windows XP und Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="23b06-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="23b06-121">Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Klasse oder Methode erforderlich sind, finden Sie im Abschnitt Weitere Informationen in der Dokumentation für die Klasse oder Methode.</span><span class="sxs-lookup"><span data-stu-id="23b06-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="23b06-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="23b06-122">In this section</span></span>

| <span data-ttu-id="23b06-123">Thema</span><span class="sxs-lookup"><span data-stu-id="23b06-123">Topic</span></span>                                                    | <span data-ttu-id="23b06-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23b06-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="23b06-125">Übersicht</span><span class="sxs-lookup"><span data-stu-id="23b06-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="23b06-126">Allgemeine Informationen zu GDI+.</span><span class="sxs-lookup"><span data-stu-id="23b06-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="23b06-127">Genutzt</span><span class="sxs-lookup"><span data-stu-id="23b06-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="23b06-128">Aufgaben und Beispiele mit GDI+.</span><span class="sxs-lookup"><span data-stu-id="23b06-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="23b06-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="23b06-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="23b06-130">Dokumentation für die klassenbasierte API von GDI+ C++.</span><span class="sxs-lookup"><span data-stu-id="23b06-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="23b06-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23b06-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b06-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="23b06-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="23b06-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23b06-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="23b06-134">Windows-Abbild Erfassung</span><span class="sxs-lookup"><span data-stu-id="23b06-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="23b06-135">OpenGL</span><span class="sxs-lookup"><span data-stu-id="23b06-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="23b06-136">Windows Multimedia</span><span class="sxs-lookup"><span data-stu-id="23b06-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
