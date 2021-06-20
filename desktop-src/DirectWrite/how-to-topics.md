---
title: Themen zur Vorgehensweise (DirectWrite)
description: Sehen Sie sich die Themen zur Vorgehensweise im Programmierhandbuch zur DirectWrite-API an. DirectWrite ermöglicht Es Windows-Anwendungen, die Textbenutzeroberfläche für Benutzeroberflächen und Dokumente zu verbessern.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc35d9b92001bc8c4807f8b77434559994aaac4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406393"
---
# <a name="how-to-topics-directwrite"></a>Themen zur Vorgehensweise (DirectWrite)

Die folgenden Themen bieten eine Übersicht über die [DirectWrite-API.](direct-write-portal.md)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                                                   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausrichten von Text](how-to-align-text.md)<br/>                                                                                                                   | Sie können [DirectWrite-Text](direct-write-portal.md) mithilfe der [**SetTextAlignment-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) der [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ausrichten.<br/>                                                                                                                                                                                                               |
| [Hinzufügen von Unterstützung für mehrere Monitore](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) bietet Unterstützung für Systeme mit mehreren Monitoren. Verschiedene Monitore können unterschiedliche Pixelgeometrien (RGB, BGR oder FLAT) oder andere Attribute aufweisen. Weitere Informationen zur Pixelgeometrie finden Sie im [**Referenzthema DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) In diesem Thema erfahren Sie, wie Sie Ihrer DirectWrite-Anwendung Unterstützung für mehrere Monitore hinzufügen. <br/> |
| [Sicherstellen, dass Ihre Anwendung ordnungsgemäß auf Anzeige mit hohem DPI-Anteil angezeigt wird](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Beschreibt, wie ein Fenster erstellt wird, in dem die Anzeige ordnungsgemäß auf Anzeigen mit hohem DPI-Anteil angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Sicherstellen, dass Text mit der richtigen Leserichtung angezeigt wird](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Einige Sprachen wie Arabisch und Hebräisch erfordern eine Leserichtung von rechts nach links. Für ein [DirectWrite-Textformatobjekt](direct-write-portal.md) lautet die Standardleserichtung von links nach rechts. DirectWrite leitet die Leserichtung nicht automatisch aus dem Gebietsschema ab, daher müssen Sie dies selbst tun.<br/>                                                                                                   |
| [Aufzählen von Schriftarten](font-enumeration.md)<br/>                                                                                                               | In dieser Übersicht erfahren Sie, wie Sie die Schriftarten in der Systemschriftartauflistung nach Familiennamen aufzählen.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Ausführen von Treffertests für ein Textlayout](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Enthält ein kurzes Tutorial zum Hinzufügen von Treffertests zu einer [DirectWrite-Anwendung,](direct-write-portal.md) die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) anzeigt. <br/>                                                                                                                                                                                                                  |
| [Hinzufügen von Inlineobjekten zu einem Textlayout](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Enthält ein kurzes Tutorial zum Hinzufügen von Inlineobjekten zu einer [DirectWrite-Anwendung,](direct-write-portal.md) die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) anzeigt. <br/>                                                                                                                                                                                                                         |
| [Hinzufügen von Clientzeichnungseffekten zu einem Textlayout](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Enthält ein kurzes Tutorial zum Hinzufügen von Clientzeichnungseffekten zu einer [DirectWrite-Anwendung,](direct-write-portal.md) die Text mithilfe der [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) und eines benutzerdefinierten Textrenderers anzeigt. <br/>                                                                                                                                                                                      |



 

 

