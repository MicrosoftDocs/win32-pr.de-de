---
title: DirectWrite (DWrite)
description: Die heutigen Anwendungen müssen ein qualitativ hochwertiges Text Rendering, auflösungsunabhängige Gliederungs Schriftarten und vollständige Unterstützung für Unicode-Text und-Layouts unterstützen. DirectWrite, eine [DirectX](../directx.md) -API, bietet diese Features und vieles mehr.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2020
ms.locfileid: "104475015"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Zweck

Die heutigen Anwendungen müssen ein qualitativ hochwertiges Text Rendering, auflösungsunabhängige Gliederungs Schriftarten und vollständige Unterstützung für Unicode-Text und-Layouts unterstützen. DirectWrite, eine [DirectX](../directx.md) -API, bietet diese Features und vieles mehr.

- Ein Geräte unabhängiges textlayoutsystem zur Verbesserung der Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche.
- Hochwertiges, unter Pixel, [Microsoft ClearType](/typography/cleartype/) -Text Rendering, das [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)oder anwendungsspezifische renderingtechnologie verwenden kann.
- Hardware beschleunigter Text, bei Verwendung mit [Direct2D](rendering-by-using-direct2d.md).
- Unterstützung für mehr formatieren Text.
- Unterstützung für die erweiterten Typografiefunktionen von OpenType-Schriftarten.
- Unterstützung für Layout und Rendering von Text in allen unterstützten Sprachen.
- [GDI](interoperating-with-gdi.md)-kompatibles Layout und Rendering.

Die API unterstützt das Messen, zeichnen und Treffer Tests von Text mit mehreren Formaten. DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen, die auf der Schlüssel sprach Infrastruktur von Windows 7 aufbauen. DirectWrite stellt außerdem eine API für Glyphenrendering auf niedriger Ebene für Entwickler zur Ausführung von eigenem Layout und eigener Unicode-zu-Glyphen-Verarbeitung bereit.

> [!NOTE]
> Mit [Project Reunion](/windows/apps/project-reunion/) wird eine neue Version von DirectWrite mit dem &mdash; Namen "dwrite tecore" eingeführt, &mdash; die unter Windows-Versionen von Windows 8 bis Windows 8 ausgeführt wird. Sie öffnet die Tür, in der Sie Sie plattformübergreifend verwenden können. Weitere Informationen finden Sie unter [Übersicht über dbeschreib tecore](dwritecore-overview.md).

## <a name="run-time-requirements"></a>Laufzeitanforderungen

- Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Platt Form Update für Windows Vista
- Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Neues in DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Im folgenden finden Sie einige der neuen Ergänzungen zu DirectWrite. <br/> |
| [Programmierhandbuch](programming-guide.md)<br/> | Die folgenden Themen bieten eine Übersicht über die DirectWrite-API.<br/> |
| [API-Referenz](reference.md)<br/> | Beschreibt die DirectWrite-API.<br/> |
| [Beispielcode](samples.md)<br/> | Dieser Abschnitt enthält Informationen zu Beispielprogrammen für DirectWrite.<br/> |
