---
title: Visuelle Stile
description: Dieser Abschnitt bietet eine Übersicht über visuelle Stile und erläutert, wie Sie Ihre Anwendung für deren Verwendung konfigurieren.
ms.assetid: 9b135ccb-5e36-4657-b79c-689201047430
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bb1f8ff84f2c9f4d268ec8b50f8e7688519ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036801"
---
# <a name="visual-styles"></a><span data-ttu-id="fe5fc-103">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="fe5fc-103">Visual Styles</span></span>

## <a name="purpose"></a><span data-ttu-id="fe5fc-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="fe5fc-104">Purpose</span></span>

<span data-ttu-id="fe5fc-105">*Visuelle Stile* ändern das Aussehen allgemeiner Steuerelemente basierend auf dem vom Benutzer ausgewählten Design.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-105">*Visual styles* changes the appearance of common controls based on the theme chosen by the user.</span></span> <span data-ttu-id="fe5fc-106">Vor Windows 8 müssen Sie die Anwendung speziell für die Verwendung visueller Stile konfigurieren. Andernfalls werden die allgemeinen Steuerelemente der Anwendung immer im Stil gerendert, der dem klassischen Windows-Design zugeordnet ist, unabhängig vom aktuell ausgewählten Design.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-106">Prior to Windows 8, you must specifically configure your application to use visual styles; otherwise, the application's common controls are always rendered in the style associated with the Windows Classic theme, regardless of the currently selected theme.</span></span> <span data-ttu-id="fe5fc-107">In Windows 8 können visuelle Stile nicht deaktiviert werden, der klassische Modus von Windows ist nicht mehr vorhanden, und der Modus für hohe Kontraste wurde geändert, um mit visuellen Stilen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-107">In Windows 8, visual styles can't be turned off, Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span>

<span data-ttu-id="fe5fc-108">Dieser Abschnitt bietet eine Übersicht über visuelle Stile und erläutert, wie Sie Ihre Anwendung für deren Verwendung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-108">This section provides an overview of visual styles and explains how to configure your application to use them.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fe5fc-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="fe5fc-109">Developer audience</span></span>

<span data-ttu-id="fe5fc-110">Visuelle Stile sind für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-110">Visual styles are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="fe5fc-111">Im Allgemeinen benötigen Entwickler einen mittleren Einblick in die Programmier Konzepte der Benutzeroberfläche, die Windows-API-Programmierung und Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-111">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fe5fc-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-112">Run-time requirements</span></span>

<span data-ttu-id="fe5fc-113">Windows Vista und spätere Betriebssysteme.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-113">Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="fe5fc-114">Visuelle Stile werden im 256-farbliche Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe5fc-114">Visual Styles are not supported in 256-color mode.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="fe5fc-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fe5fc-115">In this section</span></span>

-   [<span data-ttu-id="fe5fc-116">Neuerungen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-116">What's New</span></span>](what-s-new-for-windows-8.md)
-   [<span data-ttu-id="fe5fc-117">Übersicht über visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="fe5fc-117">Visual Styles Overview</span></span>](visual-styles-overview.md)
-   [<span data-ttu-id="fe5fc-118">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-118">Enabling Visual Styles</span></span>](cookbook-overview.md)
-   [<span data-ttu-id="fe5fc-119">Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-119">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>](using-visual-styles.md)
-   [<span data-ttu-id="fe5fc-120">Unterstützen von hoher Kontrast Designs</span><span class="sxs-lookup"><span data-stu-id="fe5fc-120">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
-   [<span data-ttu-id="fe5fc-121">Referenz zu visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-121">Visual Styles Reference</span></span>](uxctl-ref.md)

## <a name="related-topics"></a><span data-ttu-id="fe5fc-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe5fc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5fc-123">Designdatei Format</span><span class="sxs-lookup"><span data-stu-id="fe5fc-123">Theme File Format</span></span>](themesfileformat-overview.md)
</dt> <dt>

[<span data-ttu-id="fe5fc-124">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fe5fc-124">Windows Controls</span></span>](window-controls.md)
</dt> </dl>

 

 




