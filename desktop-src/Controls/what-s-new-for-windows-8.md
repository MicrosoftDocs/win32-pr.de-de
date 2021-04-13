---
title: Neuigkeiten (Windows-Steuerelemente)
description: In diesem Thema werden die Unterschiede in der Unterstützung für Designs und visuelle Stile zwischen Windows 8 und früheren Windows-Versionen beschrieben.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474820"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="a7787-103">Neuigkeiten (Windows-Steuerelemente)</span><span class="sxs-lookup"><span data-stu-id="a7787-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="a7787-104">In diesem Thema werden die Unterschiede in der Unterstützung für Designs und visuelle Stile zwischen Windows 8 und früheren Windows-Versionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7787-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="a7787-105">Über Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7787-105">Through Windows 7</span></span>

<span data-ttu-id="a7787-106">In Windows 7 sind visuelle Stile standardmäßig aktiviert, der Benutzer kann Sie jedoch deaktivieren, indem er das klassische Windows-Design oder den Designs-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7787-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="a7787-107">Wenn visuelle Stile deaktiviert sind, erhält die gesamte Benutzeroberfläche das klassische Aussehen, und die meisten Visual Styles-APIs sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7787-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="a7787-108">Der Modus "visuelle Stile aus" wurde durch Windows 7 beibehalten, um die verschiedenen Designs mit hohem Kontrast und das klassische Windows-Design zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a7787-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="a7787-109">Wenn Sie visuelle Stile und Designs mit hohem Kontrast in der gleichen Anwendung unterstützen möchten, müssen Sie in der Regel zwei separate Codepfade zum Rendern von Steuerelementen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a7787-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="a7787-110">Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="a7787-110">Windows 8 and Later</span></span>

<span data-ttu-id="a7787-111">In Windows 8 können visuelle Stile nicht durch die **Personalisierungs** Seite der **PC-Einstellungen** oder durch Ausschalten des Designs-Diensts ausgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a7787-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="a7787-112">Der klassische Windows-Modus ist nicht mehr vorhanden, und der Modus für hohe Kontraste wurde geändert, um mit visuellen Stilen arbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="a7787-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="a7787-113">Aufgrund dieser Änderungen benötigen Anwendungen, die nur auf Windows 8 abzielen, nicht mehr zwei separate Codepfade, um visuelle Stile und Designs mit hohem Kontrast zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a7787-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="a7787-114">Visuelle Stile in Windows 8 enthalten abwärts Kompatibilitäts Unterstützung für den klassischen Windows-themenmodus.</span><span class="sxs-lookup"><span data-stu-id="a7787-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="a7787-115">Alle Benutzeroberflächen-Renderingcodes, die auf früheren Versionen funktionieren, funktionieren unter Windows 8 weiterhin ohne Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a7787-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="a7787-116">Wenn die Anwendung in Windows 8 die Designs mit hohem Kontrast, die auf visuellen Stilen basieren, unterstützen soll, müssen Sie die Windows 8-GUID in den Kompatibilitäts Abschnitt Ihres Anwendungs Manifests einschließen.</span><span class="sxs-lookup"><span data-stu-id="a7787-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="a7787-117">Andernfalls geht das System davon aus, dass die Anwendung auf eine frühere Version ausgelegt ist, und rendert den Client Bereich durch Simulieren der klassischen Windows-Designs mit hohem Kontrast.</span><span class="sxs-lookup"><span data-stu-id="a7787-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="a7787-118">Weitere Informationen finden Sie [unter unterstützen von hoher Kontrast](supporting-high-contrast-themes.md)Designs.</span><span class="sxs-lookup"><span data-stu-id="a7787-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="a7787-119">Wie in früheren Versionen unterstützt Windows 8 sowohl Version 5 als auch Version 6 der allgemeinen Steuerelemente, wobei Version 5 die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="a7787-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="a7787-120">Da nur Version 6 visuelle Stile unterstützt, müssen Sie im Anwendungs Manifest Version 6 angeben, wenn visuelle Stile auf die allgemeinen Steuerelemente im Client Bereich Ihrer Anwendung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7787-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="a7787-121">Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a7787-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7787-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7787-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7787-123">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="a7787-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="a7787-124">Unterstützen von hoher Kontrast Designs</span><span class="sxs-lookup"><span data-stu-id="a7787-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="a7787-125">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="a7787-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="a7787-126">Übersicht über visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="a7787-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




