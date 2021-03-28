---
description: Die folgenden Funktionen werden mit Pinseln verwendet.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Pinsel Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528394"
---
# <a name="brush-functions-windows-gdi"></a>Pinsel Funktionen (Windows GDI)

Die folgenden Funktionen werden mit Pinseln verwendet.



| Funktion                                                   | BESCHREIBUNG                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**"Kreatebrushindirekte"**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Erstellt einen Pinsel mit einem angegebenen Stil, einer angegebenen Farbe und einem angegebenen Muster. |
| [**"Kreatedibpatternbrushpt"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Erstellt einen Pinsel mit dem Muster aus einem DIB.                |
| [**"Kreatehatchbrush"**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Erstellt einen Pinsel mit einem Schraffurmuster und einer Farbe.             |
| [**"Kreatepatternbrush"**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Erstellt einen Pinsel mit einem Bitmapmuster.                      |
| [**"Kreatesolidbrush"**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Erstellt einen Pinsel mit einer voll Tonfarbe.                         |
| [**Getbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Ruft den Pinsel Ursprung für einen Gerätekontext ab.                 |
| [**Getsyscolorbrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Ruft ein Handle für einen Pinsel ab, der einem Farbindex entspricht. |
| [**Patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Zeichnet ein Rechteck.                                         |
| [**Setbrushorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Legt den Pinsel Ursprung für einen Gerätekontext fest.                 |
| [**Setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Legt die Farbe des aktuellen Gerätekontext Pinsels fest.               |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen werden nur aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.

[**"Kreatedibpatternbrush"**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



