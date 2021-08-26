---
title: API zur Vergrößerung
description: Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 2a6c7a7ffb103b39c506c41b6b7b88f82319685226aff0d479558977caa9d46b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998433"
---
# <a name="magnification-api"></a>API zur Vergrößerung

## <a name="purpose"></a>Zweck

Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.

## <a name="where-applicable"></a>Anwendungsbereich

Mithilfe der Vergrößerungs-API können Entwickler Windows-basierte Hilfstechnologieanwendungen erstellen, die den Bildschirm vergrößern und Farbeffekte auf den vergrößerten Bildschirminhalt anwenden. Für Benutzer mit sehlosem Sehen können die vergrößerte Bildgröße und die Farbeffekte dazu beitragen, den Computer einfacher zu sehen und zu verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

Die Vergrößerungs-API ist in erster Linie für C- und C++-Entwickler konzipiert, die Windows programmieren und mit Konzepten der Grafikprogrammierung vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die erste Version der Vergrößerungs-API wird unter Windows Vista-Betriebssystemen und höher unterstützt. Ein zweites Release fügt Vollbildvergrößerungsfunktionen hinzu und wird auf Windows 8 und höher unterstützt.

Die API wird von Magnification.dll. Um Ihre Anwendung zu kompilieren, schließen Sie Magnification.h ein, und verknüpfen Sie magnification.lib.

> [!Note]  
> Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Vergrößerungsanwendung wird auf 64-Bit-Anwendungen Windows.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|:---|:---|
| [Übersicht über die Vergrößerungs-API](magapi-intro.md)<br/> | In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie sie in einer Anwendung verwendet wird.<br/> |
| [Referenz](entry-magapi-ref.md)<br/>  | Dieser Abschnitt enthält Referenzinformationen für die Vergrößerungs-API.<br/>|
| [Beispiele](magapi-samples-entry.md)<br/> | Die folgende Beispielanwendung veranschaulicht die Verwendung der Vergrößerungs-API, um eine Vollbildlupe zu erstellen, die den gesamten Bildschirm vergrößert, und eine Bildschirmlupe mit Fenstern, die einen Teil des Bildschirms in einem Fenster vergrößert und anzeigt.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Microsoft-Website für](https://www.microsoft.com/accessibility/) [Barrierefreiheit, Barrierefreiheit in Windows 10](/windows/apps/accessibility)
