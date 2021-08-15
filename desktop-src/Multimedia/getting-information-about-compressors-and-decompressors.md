---
title: Abrufen von Informationen zu Komprimierungs- und Dekomprimierern
description: Abrufen von Informationen zu Komprimierungs- und Dekomprimierern
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Videokomprimierungs-Manager (Video Compression Manager, VCM), Abrufen von Informationen zu Komprimierungsdateien
- VCM (Videokomprimierungs-Manager), Abrufen von Informationen zu Komprimierung
- ICGetInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678611"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Abrufen von Informationen zu Komprimierungs- und Dekomprimierern

Ihre Anwendung kann die ICGetInfo-Funktion verwenden, um allgemeine Informationen zu einem Bzw. [**Dekomprimierer zu**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) erhalten. Diese Funktion füllt eine [**ICINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-icinfo) mit Informationen zum Bzw. Dekomprimierer auf. Ihre Anwendung muss den Arbeitsspeicher für die **ICINFO-Struktur** zuordnen und einen Zeiger darauf in **ICGetInfo übergeben.** Die Flags in der **ICINFO-Struktur** enthalten die nützlichsten Informationen zu den Funktionen einer Bzw. eines Dekomprimierers, es sei denn, Ihre Anwendung sucht nach einem bestimmten Bzw. Dekomprimierer.

Um die Standard-Keyframerate und den Standardqualitätswert einer Bzw. eines Dekomprimierers zu erhalten, kann Ihre Anwendung die [**ICM \_ GETDEFAULTKEYFRAMERATE-**](icm-getdefaultkeyframerate.md) und [**ICM \_ GETDEFAULTQUALITY-Nachrichten**](icm-getdefaultquality.md) senden (oder die [**Makros ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) verwenden).

Um das beste Anzeigeformat einer Bzw. eines Dekomprimierers zu ermitteln, kann Ihre Anwendung die [**ICGetDisplayFormat-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) verwenden.

Um zu ermitteln, ob ein Bzw. ein Dekomprimierer ein Dialogfeld "About" anzeigen kann, senden Sie die ICM [**\_ ABOUT-Nachricht**](icm-about.md) (oder verwenden Sie das [**ICQueryAbout-Makro).**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) Sie können auch das Dialogfeld About (Informationen) einer Bzw. eines Dekomprimierers anzeigen, indem Sie die ICM ABOUT-Nachricht senden und den Wert des \_ *wParam-Parameters* ändern (oder indem Sie das [**ICAbout-Makro**](/windows/desktop/api/Vfw/nf-vfw-icabout) verwenden).

 

 




