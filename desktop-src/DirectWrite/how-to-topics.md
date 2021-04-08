---
title: Themen zur Vorgehensweise (DirectWrite)
description: Die folgenden Themen bieten eine Übersicht über die DirectWrite-API.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26bbb4500ab016fbf5a5a59f6b551030e28dd1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039984"
---
# <a name="how-to-topics-directwrite"></a>Themen zur Vorgehensweise (DirectWrite)

Die folgenden Themen bieten eine Übersicht über die [DirectWrite](direct-write-portal.md) -API.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausrichten von Text](how-to-align-text.md)<br/>                                                                                                                   | Sie können [DirectWrite](direct-write-portal.md) -Text mithilfe der [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) -Methode der [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle ausrichten.<br/>                                                                                                                                                                                                               |
| [Vorgehensweise beim Hinzufügen von Unterstützung für mehrere Monitore](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) bietet Unterstützung für Systeme mit mehreren Monitoren. Verschiedene Monitore verfügen möglicherweise über unterschiedliche Pixelgeometrie (RGB, BGR oder Flat) oder andere Attribute. Weitere Informationen zur Pixelgeometrie finden Sie im Thema zum [**dwrite \_ Pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) -Referenz Thema. In diesem Thema wird gezeigt, wie Sie Ihrer DirectWrite-Anwendung Unterstützung für mehrere Monitore hinzufügen. <br/> |
| [So stellen Sie sicher, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Hier wird beschrieben, wie ein Fenster erstellt wird, das auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Sicherstellen, dass Text mit der richtigen Leserichtung angezeigt wird](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Einige Sprachen, z. b. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links. Die für ein [DirectWrite](direct-write-portal.md) -Textformat Objekt, die Standard Leserichtung ist von links nach rechts. DirectWrite leitet die Leserichtung nicht automatisch aus dem Gebiets Schema ab, sodass Sie dies selbst tun müssen.<br/>                                                                                                   |
| [Auflisten von Schriftarten](font-enumeration.md)<br/>                                                                                                               | In dieser Übersicht wird gezeigt, wie die Schriftarten in der System Schriftart Auflistung nach dem Familiennamen aufgelistet werden.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Ausführen von Treffer Tests für ein Text Layout](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Bietet ein kurzes Tutorial zum Hinzufügen von Treffer Tests zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt. <br/>                                                                                                                                                                                                                  |
| [Vorgehensweise beim Hinzufügen von Inline Objekten zu einem Text Layout](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Bietet ein kurzes Tutorial zum Hinzufügen von Inline Objekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die Text mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle anzeigt. <br/>                                                                                                                                                                                                                         |
| [Hinzufügen von Client Zeichnungs Effekten zu einem Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Bietet ein kurzes Tutorial zum Hinzufügen von Client Zeichnungs Effekten zu einer [DirectWrite](direct-write-portal.md) -Anwendung, die mithilfe der [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle und einem benutzerdefinierten TextRenderer Text anzeigt. <br/>                                                                                                                                                                                      |



 

 

