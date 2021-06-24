---
title: DirectWrite (DWrite)
description: Heutige Anwendungen müssen qualitativ hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und vollständige Unicode-Text- und Layoutunterstützung unterstützen. DirectWrite, eine [DirectX-API,](../directx.md) bietet diese Features und vieles mehr.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587941"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Zweck

Heutige Anwendungen müssen qualitativ hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und vollständige Unicode-Text- und Layoutunterstützung unterstützen. DirectWrite, eine [DirectX-API,](../directx.md) bietet diese Features und vieles mehr.

- Ein geräteunabhängiges Textlayoutsystem, das die Lesbarkeit von Text in Dokumenten und auf der Benutzeroberfläche verbessert.
- Qualitativ hochwertiges, untergeordnetes Pixel, Microsoft ClearType-Textrendering, das [GDI-,](interoperating-with-gdi.md) [Direct2D-](rendering-by-using-direct2d.md)oder anwendungsspezifische Renderingtechnologie verwenden kann. [](/typography/cleartype/)
- Hardwarebeschleunigte Text, wenn er mit [Direct2D](rendering-by-using-direct2d.md)verwendet wird.
- Unterstützung für Mehrformattext.
- Unterstützung für die erweiterten Typografiefeatures von OpenType-Schriftarten.
- Unterstützung für das Layout und Rendering von Text in allen unterstützten Sprachen.
- [GDI-kompatibles](interoperating-with-gdi.md)Layout und Rendering.

Die API unterstützt das Messen, Zeichnen und Treffertesten von Mehrformattext. DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen und baut auf der schlüsselsprachlichen Infrastruktur in Windows 7 auf. DirectWrite stellt außerdem eine API für Glyphenrendering auf niedriger Ebene für Entwickler zur Ausführung von eigenem Layout und eigener Unicode-zu-Glyphen-Verarbeitung bereit.

> [!NOTE]
> [Das Windows App SDK](/windows/apps/windows-app-sdk/) führt eine neue Version von DirectWrite &mdash; mit dem Namen DWriteCore &mdash; ein, die unter Windows-Versionen bis hin zu Windows 8 ausgeführt wird, und öffnet Ihnen die Möglichkeit, sie plattformübergreifend zu verwenden. Weitere Informationen finden Sie unter [Übersicht über DWriteCore.](dwritecore-overview.md)

## <a name="run-time-requirements"></a>Laufzeitanforderungen

- Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Plattformupdate für Windows Vista
- Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Plattformupdate für Windows Server 2008

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Neuerungen in DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Hier sind einige der neuen Ergänzungen zu DirectWrite. <br/> |
| [Programmierhandbuch](programming-guide.md)<br/> | Die folgenden Themen bieten eine Übersicht über die DirectWrite-API.<br/> |
| [API-Referenz](reference.md)<br/> | Beschreibt die DirectWrite-API.<br/> |
| [Beispielcode](samples.md)<br/> | Dieser Abschnitt enthält Informationen zu Beispielprogrammen für DirectWrite.<br/> |
