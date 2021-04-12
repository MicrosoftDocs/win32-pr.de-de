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
# <a name="ink-presenter"></a>Ink Presenter

Mithilfe der Ink Presenter-APIs können Microsoft Win32-apps Eingaben, Verarbeitungsvorgänge und Rendering von frei Hand Eingaben (Standard und geändert) über ein [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Objekt verwalten, das in die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app eingefügt wurde.

> [!Note]
>
> Standard Freihand Eingabe (Stift Tipp oder radierertipp/Schaltfläche) wird nicht mit einem sekundären Profil geändert, wie z. b. einer Stift-Taste, der rechten Maustaste oder ähnlich.

Universelle Windows-Plattform-Apps (UWP), die Extensible Application Markup Language (XAML) verwenden, stellen diese Funktionalität über ein [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) -Steuerelement zusammen mit einem [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Objekt bereit, das eine Verbindung mit der visuellen XAML [directcomposition](../directcomp/directcomposition-portal.md) -Struktur herstellt. Weitere Details finden Sie unter [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions).

Der [Ink-Renderer](ink-renderer.md) ist für die Verwendung durch universelle Windows-App konzipiert, die an der Bereitstellung von XAML-basierten [](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) -Funktionen in nativen Win32-apps interessiert sind

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Ink Presenter-Klassen](ink-presenter-classes.md)<br/>       | Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Ink Presenter-Klassen. <br/>    |
| [Ink Presenter-Schnittstellen](ink-presenter-interfaces.md)<br/> | Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Ink Presenter-Schnittstellen. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

[Ink Presenter](ink-presenter.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift [Analyse Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel zum Einfügen](/samples/microsoft/windows-universal-samples/simpleink/), Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung
