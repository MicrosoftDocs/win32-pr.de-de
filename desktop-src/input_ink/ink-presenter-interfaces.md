---
description: Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für Schnittstellen für die Ink-Darstellung.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Schnittstellen für die Ink-Präsentation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092390"
---
# <a name="ink-presenter-interfaces"></a>Schnittstellen für die Ink-Präsentation

Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für Schnittstellen für [die Ink-Darstellung.](ink-presenter.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Ermöglicht Ihrer App (anstelle eines [**IInkPresenterDesktop-Objekts),**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) alle ausstehenden Microsoft DirectComposition-Befehle in der visuellen [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App zu committen.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Ermöglicht Freihandeingabe, -verarbeitung und -rendering durch die Erstellung eines App-Threads, um ein [**IInkPresenterDesktop-Objekt**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) zu hosten und es in die visuelle [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der App einzufügen. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Stellt einen Freihandvorgang dar, der für einen [**IInkDesktopHost-Objektthread**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ausgeführt werden soll.<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Stellt einen [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) dar, der konfiguriert und in die visuelle [DirectComposition-Struktur](../directcomp/directcomposition-portal.md) der klassischen Windows-App eingefügt werden kann. <br/>                                        |

## <a name="related-topics"></a>Zugehörige Themen

[Ink-Presenter,](ink-presenter.md) [Stift- und Stiftinteraktionen,](/windows/uwp/design/input/pen-and-stylus-interactions) [Ink-Analysebeispiel,](/samples/microsoft/windows-universal-samples/inkanalysis/) [Einfaches Beispiel für Dasken,](/samples/microsoft/windows-universal-samples/simpleink/) [Komplexes Beispiel für Dasinken](/samples/microsoft/windows-universal-samples/complexink/)
