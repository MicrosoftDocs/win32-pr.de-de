---
title: Informationen zu Kompressoren und Dekompressoren erhalten
description: Informationen zu Kompressoren und Dekompressoren erhalten
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Videokomprimierungs-Manager (VCM), Informationen zu Kompressoren erhalten
- VCM (Videokomprimierungs-Manager), Informationen zu Kompressoren erhalten
- Icgetinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947761"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Informationen zu Kompressoren und Dekompressoren erhalten

Um allgemeine Informationen zu einem Kompressor oder Dekompressor zu erhalten, kann die Anwendung die [**icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) -Funktion verwenden. Diese Funktion füllt eine [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur mit Informationen über den Kompressor oder Dekompressor. Die Anwendung muss den Arbeitsspeicher für die **icinfo** -Struktur zuordnen und in **icgetinfo** einen Zeiger darauf übergeben. Wenn Ihre Anwendung nicht nach einem bestimmten Kompressor oder Dekompressor sucht, stellen die Flags in der **icinfo** -Struktur die nützlichsten Informationen zu den Funktionen eines Kompressors oder dekompressors bereit.

Um die standardmäßige Keyframerate und den Standardwert für die Qualität eines Kompressors oder dekompressors zu erhalten, kann Ihre Anwendung die [**ICM \_ getdefaultkeyframerate**](icm-getdefaultkeyframerate.md) -und [**ICM \_ getdefaultquality**](icm-getdefaultquality.md) -Meldungen senden (oder die Makros [**icgetdefaultkeyframerate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**icgetdefaultquality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) verwenden).

Um das beste Anzeige Format eines Kompressors oder dekompressors zu ermitteln, kann die Anwendung die [**icgetdisplayformat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) -Funktion verwenden.

Um zu ermitteln, ob ein "Info"-Dialogfeld von einem Kompressor oder Dekompressor angezeigt werden kann, senden Sie den [**ICM \_ über**](icm-about.md) die Nachricht (oder verwenden Sie das [**icqueryabout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) -Makro). Sie können auch das Dialogfeld Info eines Kompressors oder dekompressors anzeigen, indem Sie den ICM \_ über eine Nachricht senden und den Wert des *wParam* -Parameters (oder mithilfe des [**icabout**](/windows/desktop/api/Vfw/nf-vfw-icabout) -Makros) ändern.

 

 




