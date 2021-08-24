---
title: Abrufen von Informationen zu Ausstellern und Dekomprimatoren
description: Abrufen von Informationen zu Ausstellern und Dekomprimatoren
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Videokomprimierungs-Manager (VCM), Abrufen von Informationen zu Rauschen
- VCM (Videokomprimierungs-Manager),Abrufen von Informationen zu Rauschen
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
# <a name="getting-information-about-compressors-and-decompressors"></a>Abrufen von Informationen zu Ausstellern und Dekomprimatoren

Ihre Anwendung kann die [**ICGetInfo-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) verwenden, um allgemeine Informationen zu einem Entpackungs- oder Dekomprimierer zu erhalten. Diese Funktion füllt eine [**ICINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-icinfo) mit Informationen über die Füllung oder den Dekomprimierer. Ihre Anwendung muss den Arbeitsspeicher für die **ICINFO-Struktur** zuordnen und in **ICGetInfo** einen Zeiger darauf übergeben. Sofern Ihre Anwendung nicht nach einem bestimmten Konstruktor oder Dekomprimierer sucht, stellen die Flags in der **ICINFO-Struktur** die nützlichsten Informationen über die Funktionen eines Konstruktors oder Dekomprimierers bereit.

Um die Standardmäßige Keyframerate und den Standardqualitätswert eines Komprimierungs- oder Dekomprimierers abzurufen, kann Ihre Anwendung die [**ICM \_ GETDEFAULTKEYFRAMERATE-**](icm-getdefaultkeyframerate.md) und [**ICM \_ GETDEFAULTQUALITY-Nachrichten**](icm-getdefaultquality.md) senden (oder die [**ICGetDefaultKeyFrameRate-**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**ICGetDefaultQuality-Makros**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) verwenden).

Ihre Anwendung kann die [**ICGetDisplayFormat-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) verwenden, um das beste Anzeigeformat für einen Entpacker oder Dekomprimierer zu ermitteln.

Senden Sie die [**ICM \_ ABOUT-Nachricht**](icm-about.md) (oder verwenden Sie das [**IcQueryAbout-Makro),**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) um zu bestimmen, ob ein Kasten oder Dekomprimierer ein Dialogfeld "About" anzeigen kann. Sie können auch das Dialogfeld "About" eines Entpackungs- oder Dekomprimierers anzeigen, indem Sie die ICM \_ ABOUT-Nachricht senden und den Wert des *wParam-Parameters* ändern (oder indem Sie das [**ICAbout-Makro**](/windows/desktop/api/Vfw/nf-vfw-icabout) verwenden).

 

 




