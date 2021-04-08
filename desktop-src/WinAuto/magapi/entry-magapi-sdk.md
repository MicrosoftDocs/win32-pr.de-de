---
title: API zur Vergrößerung
description: Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2020
ms.locfileid: "103857975"
---
# <a name="magnification-api"></a>API zur Vergrößerung

## <a name="purpose"></a>Zweck

Mit der Vergrößerungs-API können Anwendungen den gesamten Bildschirm oder Teile des Bildschirms vergrößern und Farbeffekte anwenden.

## <a name="where-applicable"></a>Anwendungsbereich

Mithilfe der Vergrößerungs-API können Entwickler Windows-basierte Hilfstechnologieanwendungen erstellen, die den Bildschirm vergrößern und Farbeffekte auf den vergrößerten Bildschirminhalt anwenden. Für Benutzer mit Sehbehinderung können die vergrößerten Bildgrößen und Farbeffekte dazu beitragen, den Computer leichter zu erkennen und zu verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

Die Vergrößerungs-API wurde hauptsächlich für C-und C++-Entwickler entwickelt, die sich mit der Windows-Programmierung vertraut machen und mit den Konzepten der Grafik Programmierung

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die erste Version der Vergrößerungs-API wird unter Windows Vista und höheren Betriebssystemen unterstützt. Eine zweite Version bietet Funktionen zur voll Bildvergrößerung und wird unter Windows 8 und höher unterstützt.

Die API wird von Magnification.dll unterstützt. Wenn Sie die Anwendung kompilieren möchten, schließen Sie "Vergrößerung. h" ein, und verknüpfen Sie Sie mit "

> [!Note]  
> Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Bildschirmlupe wird auf 64-Bit-Fenstern nicht ordnungsgemäß ausgeführt.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|:---|:---|
| [Übersicht über die Vergrößerung](magapi-intro.md)<br/> | In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird.<br/> |
| [Verweis](entry-magapi-ref.md)<br/>  | Dieser Abschnitt enthält Referenzinformationen für die Vergrößerungs-API.<br/>|
| [Beispiele](magapi-samples-entry.md)<br/> | Die folgende Beispielanwendung veranschaulicht, wie die Vergrößerungs-API verwendet wird, um eine Vollbild-Bildschirmlupe zu erstellen, die den gesamten Bildschirm vergrößert, und eine Bildschirmlupe, die einen Teil des Bildschirms in einem Fenster vergrößert und anzeigt.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Microsoft-Website für Barrierefreiheit](https://www.microsoft.com/accessibility/), [Barrierefreiheit in Windows 10](/windows/apps/accessibility)
