---
title: Themen zur Funktionsweise (DirectWrite)
description: Sehen Sie sich die Anleitungsthemen im DirectWrite API-Programmierhandbuch an. DirectWrite ermöglicht Windows, die Textoberfläche für Benutzeroberfläche und Dokumente zu verbessern.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42848fbf00e099926763f0db54338f3a87ff583782b939f8250a1aabb2b73ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048860"
---
# <a name="how-to-topics-directwrite"></a>Themen zur Funktionsweise (DirectWrite)

Die folgenden Themen bieten eine Übersicht über [die](direct-write-portal.md) DirectWrite-API.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausrichten von Text](how-to-align-text.md)<br/>                                                                                                                   | Sie können [DirectWrite](direct-write-portal.md) Text ausrichten, indem Sie die [**SetTextAlignment-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) der [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) verwenden.<br/>                                                                                                                                                                                                               |
| [Hinzufügen von Unterstützung für mehrere Monitore](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) unterstützt Systeme mit mehreren Monitoren. Verschiedene Monitore können unterschiedliche Pixelgeometrie (RGB, BGR oder FLAT) oder andere Attribute haben. Weitere Informationen zur Pixelgeometrie finden Sie im [**DWRITE \_ PIXEL \_ GEOMETRY-Referenzthema.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) In diesem Thema erfahren Sie, wie Sie Ihrer Anwendung Unterstützung für mehrere Monitore DirectWrite hinzufügen. <br/> |
| [So stellen Sie sicher, dass Ihre Anwendung ordnungsgemäß auf Bildschirmen mit hohem DPI-Leistung angezeigt wird](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Beschreibt, wie ein Fenster erstellt wird, das auf Bildschirmen mit hohem DPI-Grad ordnungsgemäß angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Sicherstellen, dass Text mit der richtigen Leserichtung angezeigt wird](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Einige Sprachen, z. B. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links. Der für [](direct-write-portal.md) ein DirectWrite-Textformatobjekt ist die Standardleserichtung von links nach rechts. DirectWrite die Leserichtung nicht automatisch aus dem -Locale abgeleitet, daher müssen Sie dies selbst tun.<br/>                                                                                                   |
| [Aufzählen von Schriftarten](font-enumeration.md)<br/>                                                                                                               | In dieser Übersicht wird gezeigt, wie die Schriftarten in der Auflistung der Systemschriftarten nach Familienname aufzählt werden.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Ausführen von Treffertests für ein Textlayout](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Enthält ein kurzes Tutorial zum Hinzufügen [](direct-write-portal.md) von Treffertests zu einer DirectWrite Anwendung, die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) anzeigt. <br/>                                                                                                                                                                                                                  |
| [Hinzufügen von Inlineobjekten zu einem Textlayout](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Enthält ein kurzes Tutorial zum [](direct-write-portal.md) Hinzufügen von Inlineobjekten zu DirectWrite Anwendung, die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) anzeigt. <br/>                                                                                                                                                                                                                         |
| [Hinzufügen von Clientzeichnungseffekten zu einem Textlayout](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Enthält ein kurzes Tutorial zum [](direct-write-portal.md) Hinzufügen von Clientzeichnungseffekten zu einer DirectWrite-Anwendung, die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) und eines benutzerdefinierten Textrenderers anzeigt. <br/>                                                                                                                                                                                      |



 

 

