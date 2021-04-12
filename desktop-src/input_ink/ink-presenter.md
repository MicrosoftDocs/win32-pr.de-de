---
description: Die InkPresenter-APIs ermöglichen Microsoft Win32-Apps die Verwaltung von Eingabe, Verarbeitung und Rendering der Freihandeingabe (Standard und angepasst) über ein InkPresenter-Objekt in der visuellen DirectComposition-Struktur der App.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Ink Presenter
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217038"
---
# <a name="ink-presenter"></a><span data-ttu-id="071e9-103">Ink Presenter</span><span class="sxs-lookup"><span data-stu-id="071e9-103">Ink presenter</span></span>

<span data-ttu-id="071e9-104">Mithilfe der Ink Presenter-APIs können Microsoft Win32-apps Eingaben, Verarbeitungsvorgänge und Rendering von frei Hand Eingaben (Standard und geändert) über ein [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Objekt verwalten, das in die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="071e9-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="071e9-105">Standard Freihand Eingabe (Stift Tipp oder radierertipp/Schaltfläche) wird nicht mit einem sekundären Profil geändert, wie z. b. einer Stift-Taste, der rechten Maustaste oder ähnlich.</span><span class="sxs-lookup"><span data-stu-id="071e9-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="071e9-106">Universelle Windows-Plattform-Apps (UWP), die Extensible Application Markup Language (XAML) verwenden, stellen diese Funktionalität über ein [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) -Steuerelement zusammen mit einem [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Objekt bereit, das eine Verbindung mit der visuellen XAML [directcomposition](../directcomp/directcomposition-portal.md) -Struktur herstellt.</span><span class="sxs-lookup"><span data-stu-id="071e9-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="071e9-107">Weitere Details finden Sie unter [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions).</span><span class="sxs-lookup"><span data-stu-id="071e9-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="071e9-108">Der [Ink-Renderer](ink-renderer.md) ist für die Verwendung durch universelle Windows-App konzipiert, die an der Bereitstellung von XAML-basierten [](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Funktionen in nativen Win32-apps interessiert sind</span><span class="sxs-lookup"><span data-stu-id="071e9-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="071e9-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="071e9-109">In this section</span></span>



| <span data-ttu-id="071e9-110">Thema</span><span class="sxs-lookup"><span data-stu-id="071e9-110">Topic</span></span>                                                               | <span data-ttu-id="071e9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="071e9-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="071e9-112">Ink Presenter-Klassen</span><span class="sxs-lookup"><span data-stu-id="071e9-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="071e9-113">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Ink Presenter-Klassen.</span><span class="sxs-lookup"><span data-stu-id="071e9-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="071e9-114">Ink Presenter-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="071e9-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="071e9-115">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Ink Presenter-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="071e9-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="071e9-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="071e9-116">Related topics</span></span>

<span data-ttu-id="071e9-117">[Ink Presenter](ink-presenter.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift [Analyse Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel zum Einfügen](/samples/microsoft/windows-universal-samples/simpleink/), Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung</span><span class="sxs-lookup"><span data-stu-id="071e9-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
