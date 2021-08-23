---
description: Die folgenden Funktionen werden mit Pinseln verwendet.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Pinselfunktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f122592e1f13186253b349089706686d352460a364e405c404fd326f64989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849290"
---
# <a name="brush-functions-windows-gdi"></a>Pinselfunktionen (Windows GDI)

Die folgenden Funktionen werden mit Pinseln verwendet.



| Funktion                                                   | Beschreibung                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Erstellt einen Pinsel mit einem angegebenen Stil, einer angegebenen Farbe und einem angegebenen Muster. |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Erstellt einen Pinsel mit dem Muster aus einem DIB                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Erstellt einen Pinsel mit Schraffierungsmuster und Farbe             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Erstellt einen Pinsel mit einem Bitmapmuster                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Erstellt einen Pinsel mit einer Volltonfarbe.                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Ruft den Pinsel-Ursprung für einen Gerätekontext ab.                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Ruft ein Handle für einen Pinsel ab, der einem Farbindex entspricht. |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Zeichnet ein Rechteck                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Legt den Pinsel-Ursprung für einen Gerätekontext fest.                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Legt die aktuelle Gerätekontextpinselfarbe fest.               |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen werden nur zur Kompatibilität mit 16-Bit-Versionen von Windows.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



