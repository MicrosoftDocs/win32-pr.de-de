---
title: Windows Color System (WCS)
description: Farb Verwaltungs Schemas werden in Microsoft Windows-Betriebssystemen implementiert, um das Rendering von Farb Inhalten in allen Formen der digitalen Kommunikation zu verbessern. Das Farb Verwaltungs Schema, das ab Windows 2000, Windows XP und Windows Server 2003 verwendet wird, wird als Bild Farbverwaltung (Image Color Management, ICM) 2,0 bezeichnet. Das Farb Verwaltungs Schema, das ab Windows Vista verwendet wird, heißt Windows Color System (WCS) 1,0. Das WCS 1,0-Farb Verwaltungs Schema ist eine supermenge von ICM 2,0-APIs und-Funktionen.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363897"
---
# <a name="windows-color-system"></a><span data-ttu-id="ce007-105">Windows Color System (WCS)</span><span class="sxs-lookup"><span data-stu-id="ce007-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="ce007-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="ce007-106">Purpose</span></span>

<span data-ttu-id="ce007-107">Farb Verwaltungs Schemas werden in Microsoft Windows-Betriebssystemen implementiert, um das Rendering von Farb Inhalten in allen Formen der digitalen Kommunikation zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ce007-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="ce007-108">Das Farb Verwaltungs Schema, das ab Windows 2000, Windows XP und Windows Server 2003 verwendet wird, wird als Bild Farbverwaltung (Image Color Management, ICM) 2,0 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ce007-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="ce007-109">Das Farb Verwaltungs Schema, das ab Windows Vista verwendet wird, heißt Windows Color System (WCS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="ce007-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="ce007-110">Das WCS 1,0-Farb Verwaltungs Schema ist eine supermenge von ICM 2,0-APIs und-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ce007-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ce007-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="ce007-111">Where applicable</span></span>

<span data-ttu-id="ce007-112">ICM kann in allen Anwendungen unter Windows 2000 und neueren Betriebssystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce007-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="ce007-113">WCS kann in allen Anwendungen unter Windows Vista und höheren Betriebssystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce007-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ce007-114">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="ce007-114">Developer audience</span></span>

<span data-ttu-id="ce007-115">Die WCS-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="ce007-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="ce007-116">Kenntnisse über die grafische Benutzeroberfläche von Windows, die Nachrichten gesteuerte Architektur und ein funktionierendes Wissen der Farb Verwaltungs Konzepte sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce007-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ce007-117">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="ce007-117">Run-time requirements</span></span>

<span data-ttu-id="ce007-118">Für Anwendungen, die die ICM-API verwenden, ist Windows 2000 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce007-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="ce007-119">Für Anwendungen, die die WCS-API verwenden, ist Windows Vista oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ce007-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="ce007-120">Informationen zu bestimmten Laufzeitinformationen zu einer Funktion finden Sie im Abschnitt "Anforderungen" der Referenzseite für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="ce007-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce007-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ce007-121">In this section</span></span>

-   [<span data-ttu-id="ce007-122">Sicherheitsüberlegungen: Windows Color System</span><span class="sxs-lookup"><span data-stu-id="ce007-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="ce007-123">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="ce007-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="ce007-124">Windows Color System: Schemas und Algorithmen</span><span class="sxs-lookup"><span data-stu-id="ce007-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="ce007-125">Informationen zu Windows Color System (WCS), Version 1.0</span><span class="sxs-lookup"><span data-stu-id="ce007-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="ce007-126">Verwenden von WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="ce007-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="ce007-127">Verweis</span><span class="sxs-lookup"><span data-stu-id="ce007-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="ce007-128">WCS 1.0-Glossar</span><span class="sxs-lookup"><span data-stu-id="ce007-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="ce007-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce007-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce007-130">OpenGL</span><span class="sxs-lookup"><span data-stu-id="ce007-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="ce007-131">Windows Multimedia</span><span class="sxs-lookup"><span data-stu-id="ce007-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="ce007-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="ce007-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 