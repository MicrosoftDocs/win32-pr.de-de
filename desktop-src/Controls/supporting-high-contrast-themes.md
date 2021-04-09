---
title: Unterstützen von hoher Kontrast Designs
description: In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Windows-Versionen verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8-Anwendung unterstützt werden.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858489"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="e11c5-103">Unterstützen von hoher Kontrast Designs</span><span class="sxs-lookup"><span data-stu-id="e11c5-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="e11c5-104">In diesem Thema wird die Unterstützung für Designs mit hohem Kontrast in Windows 8 mit denen früherer Windows-Versionen verglichen, und es wird erläutert, wie Designs mit hohem Kontrast in einer Windows 8-Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="e11c5-105">Dies umfasst die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="e11c5-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="e11c5-106">Übersicht über die Unterstützung von hoher Kontrast Designs</span><span class="sxs-lookup"><span data-stu-id="e11c5-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="e11c5-107">Unterstützen von hoher Kontrast Designs in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="e11c5-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="e11c5-108">Hinzufügen eines Kompatibilitäts Abschnitts zum Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="e11c5-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="e11c5-109">Erkennen von hoher Kontrast in früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="e11c5-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="e11c5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e11c5-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="e11c5-111">Übersicht über die Unterstützung von hoher Kontrast Designs</span><span class="sxs-lookup"><span data-stu-id="e11c5-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="e11c5-112">Windows 7 und frühere Versionen unterstützen zwei Designmodelle, einschließlich des klassischen Windows Classic-Modells und der aktuellen visuellen Stile.</span><span class="sxs-lookup"><span data-stu-id="e11c5-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="e11c5-113">Das klassische Windows-Modell wurde über Windows 7 vor allem zur Unterstützung der verschiedenen Designs mit hohem Kontrast beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e11c5-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="e11c5-114">Das klassische Windows-Modell weist jedoch eine Reihe von Nachteilen auf:</span><span class="sxs-lookup"><span data-stu-id="e11c5-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="e11c5-115">Keine Unterstützung für Designs, die visuelle Stile verwenden, wie z. b. Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="e11c5-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="e11c5-116">Benutzer mit Designs mit hohem Kontrast müssen die klassische Windows-Benutzeroberfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="e11c5-117">Keine Unterstützung für Benutzeroberflächen Features, die zum Ausführen von Desktopfenster-Manager (DWM) benötigt werden, wie z. b. Miniaturansichten und die voll Bild Bildschirmlupe, die in Windows 7 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e11c5-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="e11c5-118">Entwickler müssen zwei separate Codepfade verwalten, um die beiden unterschiedlichen Designmodelle zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="e11c5-119">In Windows 8 und höher werden die vorherigen Nachteile durch die folgenden Änderungen am Designmodell behandelt:</span><span class="sxs-lookup"><span data-stu-id="e11c5-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="e11c5-120">Das klassische Windows-Designmodell wird nicht mehr unterstützt, sodass Entwickler nur einen Codepfad für Anwendungen verwalten können, die nur auf Windows 8 abzielen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="e11c5-121">Da visuelle Stile und DWM in Windows 8 vorhanden sind, haben Benutzer mit hohem Kontrast Zugriff auf Features wie Miniaturansichten und die Bildschirmlupe.</span><span class="sxs-lookup"><span data-stu-id="e11c5-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="e11c5-122">Visuelle Stile unterstützen das Festlegen der Farben verschiedener Benutzeroberflächen Elemente, sodass Benutzer mit hohem Kontrast die Benutzeroberfläche anpassen können, um die individuellen Anforderungen und Vorlieben zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="e11c5-123">Windows 8 umfasst Kompatibilitäts Unterstützung für vorhandene Anwendungen, die für die Verwendung von Designs mit hohem Kontrast basierend auf dem klassischen Windows-Designmodell entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="e11c5-124">Unterstützen von hoher Kontrast Designs in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="e11c5-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="e11c5-125">Da visuelle Stile in Windows 8 im Modus mit hohem Kontrast angezeigt werden, ist die Unterstützung von Designs mit hohem Kontrast unkompliziert, solange Sie die folgenden Richtlinien beachten.</span><span class="sxs-lookup"><span data-stu-id="e11c5-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="e11c5-126">Schrift-und Steuerelement Größen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-126">Font and control sizes.</span></span> <span data-ttu-id="e11c5-127">Um sicherzustellen, dass die Benutzeroberfläche für Benutzer mit Behinderungen zugänglich ist, legen Sie Schriftart Größen entsprechend den aktuellen Design Einstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="e11c5-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="e11c5-128">Legen Sie die Größe der Steuerelemente auf mindestens die Standardgröße fest.</span><span class="sxs-lookup"><span data-stu-id="e11c5-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="e11c5-129">Ellen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-129">Colors.</span></span> <span data-ttu-id="e11c5-130">Vermeiden Sie es, hart codierte Farben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="e11c5-131">Verwenden Sie stattdessen die Systemfarben, da Sie auf dem aktuellen Design basieren.</span><span class="sxs-lookup"><span data-stu-id="e11c5-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="e11c5-132">Durch die Verwendung benutzerdefinierter Farben können die Farben in den Designs mit hohem Kontrast beeinträchtigt und überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="e11c5-133">Anwendungs Manifest.</span><span class="sxs-lookup"><span data-stu-id="e11c5-133">Application manifest.</span></span> <span data-ttu-id="e11c5-134">Für Anwendungen, die für die Arbeit mit den neuen Designs mit hohem Kontrast entwickelt wurden, sollte ein Anwendungs Kompatibilitäts Abschnitt definiert sein, der die Windows 8-Kompatibilitäts-GUIDs enthält.</span><span class="sxs-lookup"><span data-stu-id="e11c5-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="e11c5-135">Andernfalls geht Windows davon aus, dass die Anwendung auf eine ältere Version von Windows ausgelegt ist, und rendert die Benutzeroberfläche der Anwendung, indem das klassische Windows-Designmodell simuliert wird.</span><span class="sxs-lookup"><span data-stu-id="e11c5-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="e11c5-136">Hinzufügen eines Kompatibilitäts Abschnitts zum Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="e11c5-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="e11c5-137">Ein Anwendungs Manifest ist eine XML-Datei, in der die Anforderungen für eine Anwendung beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="e11c5-138">Der Kompatibilitäts Abschnitt des Manifests identifiziert die Versionen von Windows, die von der Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e11c5-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="e11c5-139">Die folgenden GUIDs werden im Kompatibilitäts Abschnitt verwendet, um die verschiedenen Versionen von Windows zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e11c5-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="e11c5-140">Version</span><span class="sxs-lookup"><span data-stu-id="e11c5-140">Version</span></span>       | <span data-ttu-id="e11c5-141">GUID</span><span class="sxs-lookup"><span data-stu-id="e11c5-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="e11c5-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e11c5-142">Windows Vista</span></span> | <span data-ttu-id="e11c5-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="e11c5-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="e11c5-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e11c5-144">Windows 7</span></span>     | <span data-ttu-id="e11c5-145">{35138b9a-5d96-4f BD-8e2d-a2440225b93a}</span><span class="sxs-lookup"><span data-stu-id="e11c5-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="e11c5-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e11c5-146">Windows 8</span></span>     | <span data-ttu-id="e11c5-147">{4a2b28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="e11c5-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="e11c5-148">Im Kompatibilitäts Abschnitt können mehrere Versionen von Windows angegeben werden, die jeweils in einem eigenen Tag enthalten sein müssen `<supportedOS/>` .</span><span class="sxs-lookup"><span data-stu-id="e11c5-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="e11c5-149">Das folgende Beispiel zeigt ein Anwendungs Manifest, das Windows 7 und Windows 8 im Kompatibilitäts Abschnitt angibt:</span><span class="sxs-lookup"><span data-stu-id="e11c5-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="e11c5-150">Wenn für eine Anwendung kein Kompatibilitäts Manifest vorhanden ist, wird davon ausgegangen, dass es sich um eine Windows Vista-Anwendung handelt, und es werden keine Design Steuerelemente im Client Bereich verwendet, wenn ein Design mit hohem Kontrast aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e11c5-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="e11c5-151">Außerdem ist das Verhalten einiger visueller Stile-Funktionen betroffen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="e11c5-152">Beispielsweise wird von [**isthmeactive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**iscompositionactive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)und [**isapptheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) false zurückgegeben, während [**openthmedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) und [**openrowmedataex**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) ein NULL-Handle zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e11c5-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="e11c5-153">Dies dient der Kompatibilitäts Unterstützung, sodass Anwendungen, die vor Windows 8 erstellt wurden, Ihre Benutzeroberfläche immer noch in demselben aussehen wie der Modus für hohe Kontraste in früheren Versionen von Windows renderingelemente darstellen können, in dem visuelle Stile nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e11c5-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="e11c5-154">Unter Windows 8 erhält die Anwendung weiterhin die Vorteile der Desktop Komposition.</span><span class="sxs-lookup"><span data-stu-id="e11c5-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="e11c5-155">Dies bedeutet beispielsweise, dass die Verwendbarkeit von Anwendungen wie z. b. der Vollbild-Bildschirmlupe nicht vom Status des Manifests einer einzelnen Anwendung abhängt.</span><span class="sxs-lookup"><span data-stu-id="e11c5-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="e11c5-156">Die Verwendbarkeits Anwendung funktioniert im Modus mit hohem Kontrast weiterhin mit einer Anwendung, die sich nicht im Manifest als Windows 8-kompatibel identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e11c5-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="e11c5-157">In den folgenden Abbildungen wird ein einfaches Dialogfeld in hohem Kontrast zu Windows 7 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e11c5-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![Dialogfeld "Benutzer-Kontrast"](images/win7-high-contrast.png)

<span data-ttu-id="e11c5-159">Dieses Bild zeigt das gleiche Dialogfeld in hohem Kontrast zu Windows 8, aber mit der Windows 7-Kompatibilität, die im Anwendungs Manifest angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="e11c5-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![Dialogfeld für den hohen Kontrast von W8](images/win7-compat.png)

<span data-ttu-id="e11c5-161">Dieses Bild zeigt das gleiche Dialogfeld in hohem Kontrast zu Windows 8, wobei Windows 8 im Anwendungs Manifest angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="e11c5-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![W8-Dialogfeld mit hohem Kontrast und Manifest](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="e11c5-163">Erkennen von hoher Kontrast in früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="e11c5-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="e11c5-164">Anwendungen, die in früheren Versionen von Windows ausgeführt werden, haben keinen Zugriff auf die neuen Designs mit hohem Kontrast.</span><span class="sxs-lookup"><span data-stu-id="e11c5-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="e11c5-165">Wenn Ihre Anwendung auf früheren Versionen von ausgeführt werden muss, sollten Sie die Unterstützung für das Rendern Ihrer Benutzeroberfläche im klassischen Windows-Designmodell in High kontra windowsst einschließen.</span><span class="sxs-lookup"><span data-stu-id="e11c5-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="e11c5-166">Die Anwendung kann ermitteln, ob ein Design mit hohem Kontrast aktiv ist, indem die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit dem **SPI \_ gethighcontrast** -Flag aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e11c5-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e11c5-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e11c5-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11c5-168">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="e11c5-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="e11c5-169">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="e11c5-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 