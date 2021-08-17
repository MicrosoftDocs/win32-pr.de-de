---
description: Die InkPresenter-APIs ermöglichen Microsoft Win32-Apps die Verwaltung von Eingabe, Verarbeitung und Rendering der Freihandeingabe (Standard und angepasst) über ein InkPresenter-Objekt in der visuellen DirectComposition-Struktur der App.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Ink-Presenter
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ccd201f39cf232e91c65d8ef15c6ccc0e8202b231818aa50d34d70f780f2d9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977020"
---
# <a name="ink-presenter"></a>Ink-Presenter

Die Ink Presenter-APIs ermöglichen Es Microsoft Win32-Apps, die Eingabe, Verarbeitung und Daseinsenderung von Ink-Eingaben (Standard und geändert) über ein [**InkPresenter-Objekt**](/uwp/api/windows.ui.input.inking.inkpresenter) zu verwalten, das in die visuelle [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App eingefügt wird.

> [!Note]
>
> Die Standardeingabe von Ink (Stifttipp oder Radierertipp/Schaltfläche) wird nicht mit einem sekundären Vorzug geändert, z. B. mit einer Stifttaste, einer rechten Maustaste oder ähnlichem.

UWP-Apps (Universal Windows Platform) mithilfe von Extensible Application Markup Language (XAML) stellen diese Funktionalität über ein [**InkCanvas-Steuerelement**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) zusammen mit einem [**InkPresenter-Objekt**](/uwp/api/windows.ui.input.inking.inkpresenter) zur Verfügung, das eine Verbindung mit der visuellen Xaml [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) herstellt. Weitere Informationen finden Sie unter [Stift- und Stiftinteraktionen.](/windows/uwp/design/input/pen-and-stylus-interactions)

[Der Ink-Renderer](ink-renderer.md) ist für die Verwendung durch Universal Windows-App-Entwickler konzipiert, die XAML-basierte [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / [**InkPresenter-Funktionen**](/uwp/api/windows.ui.input.inking.inkpresenter) in nativen Win32-Apps bereitstellen möchten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | Beschreibung                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Klassen für die Ink-Präsentation](ink-presenter-classes.md)<br/>       | Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für Ink Presenter-Klassen. <br/>    |
| [Schnittstellen für die Ink-Präsentation](ink-presenter-interfaces.md)<br/> | Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für Ink Presenter-Schnittstellen. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

[Ink-Presenter,](ink-presenter.md) [Stift- und](/windows/uwp/design/input/pen-and-stylus-interactions)Stiftinteraktionen, Beispiel für die [Ink-Analyse,](/samples/microsoft/windows-universal-samples/inkanalysis/) [Einfaches Inking-Beispiel,](/samples/microsoft/windows-universal-samples/simpleink/) [Beispiel für komplexes Inking](/samples/microsoft/windows-universal-samples/complexink/)
