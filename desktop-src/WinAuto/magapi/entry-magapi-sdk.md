---
title: API zur Vergrößerung
description: Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2020
ms.locfileid: "103857975"
---
# <a name="magnification-api"></a><span data-ttu-id="dcd88-103">API zur Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="dcd88-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="dcd88-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="dcd88-104">Purpose</span></span>

<span data-ttu-id="dcd88-105">Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd88-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="dcd88-106">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="dcd88-106">Where applicable</span></span>

<span data-ttu-id="dcd88-107">Mithilfe der Vergrößerungs-API können Entwickler Windows-basierte Hilfstechnologieanwendungen erstellen, die den Bildschirm vergrößern und Farbeffekte auf den vergrößerten Bildschirminhalt anwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd88-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="dcd88-108">Für Benutzer mit Sehbehinderung können die vergrößerten Bildgrößen und Farbeffekte dazu beitragen, den Computer leichter zu erkennen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd88-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dcd88-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="dcd88-109">Developer audience</span></span>

<span data-ttu-id="dcd88-110">Die Vergrößerungs-API wurde hauptsächlich für C-und C++-Entwickler entwickelt, die sich mit der Windows-Programmierung vertraut machen und mit den Konzepten der Grafik Programmierung</span><span class="sxs-lookup"><span data-stu-id="dcd88-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="dcd88-111">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="dcd88-111">Run-time requirements</span></span>

<span data-ttu-id="dcd88-112">Die erste Version der Vergrößerungs-API wird unter Windows Vista und höheren Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd88-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="dcd88-113">Eine zweite Version bietet Funktionen zur voll Bildvergrößerung und wird unter Windows 8 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd88-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="dcd88-114">Die API wird von Magnification.dll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcd88-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="dcd88-115">Wenn Sie die Anwendung kompilieren möchten, schließen Sie "Vergrößerung. h" ein, und verknüpfen Sie Sie mit "</span><span class="sxs-lookup"><span data-stu-id="dcd88-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="dcd88-116">Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Bildschirmlupe wird auf 64-Bit-Fenstern nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcd88-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dcd88-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dcd88-117">In this section</span></span>

| <span data-ttu-id="dcd88-118">Thema</span><span class="sxs-lookup"><span data-stu-id="dcd88-118">Topic</span></span> | <span data-ttu-id="dcd88-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcd88-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="dcd88-120">Übersicht über die Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="dcd88-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="dcd88-121">In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcd88-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="dcd88-122">Verweis</span><span class="sxs-lookup"><span data-stu-id="dcd88-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="dcd88-123">Dieser Abschnitt enthält Referenzinformationen für die Vergrößerungs-API.</span><span class="sxs-lookup"><span data-stu-id="dcd88-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="dcd88-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcd88-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="dcd88-125">Die folgende Beispielanwendung veranschaulicht, wie die Vergrößerungs-API verwendet wird, um eine Vollbild-Bildschirmlupe zu erstellen, die den gesamten Bildschirm vergrößert, und eine Bildschirmlupe, die einen Teil des Bildschirms in einem Fenster vergrößert und anzeigt.</span><span class="sxs-lookup"><span data-stu-id="dcd88-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="dcd88-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dcd88-126">Related topics</span></span>

<span data-ttu-id="dcd88-127">[Microsoft-Website für Barrierefreiheit](https://www.microsoft.com/accessibility/), [Barrierefreiheit in Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="dcd88-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
