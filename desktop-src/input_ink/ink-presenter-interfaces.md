---
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Ink Presenter-Schnittstellen.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Ink Presenter-Schnittstellen
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360480"
---
# <a name="ink-presenter-interfaces"></a>Ink Presenter-Schnittstellen

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Ink Presenter](ink-presenter.md) -Schnittstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**Iinkcommitrequesthandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Ermöglicht der APP (anstelle eines [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekts) das Commit aller ausstehenden Microsoft directcomposition-Befehle an die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app.<br/>   |
| [**Iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Ermöglicht die Eingabe, Verarbeitung und das Rendering von Hand Eingaben durch die Erstellung eines App-Threads zum Hosten eines [**iinkpresenterdesktop-**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) Objekts und Einfügen in die visuelle [directcomposition](../directcomp/directcomposition-portal.md) -Struktur der app. <br/> |
| [**Iinkhostworkitem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Stellt einen frei Hand Vorgang dar, der auf einem [**iinkdesktophost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) -Objekt Thread ausgeführt werden soll.<br/>                                                                                                                                                  |
| [**Iinkpresenterdesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Stellt eine [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) dar, die konfiguriert und in den visuellen [directcomposition](../directcomp/directcomposition-portal.md) -Baum der klassischen Windows-app eingefügt werden kann. <br/>                                        |

## <a name="related-topics"></a>Zugehörige Themen

[Ink Presenter](ink-presenter.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift [Analyse Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel zum Einfügen](/samples/microsoft/windows-universal-samples/simpleink/), Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung
