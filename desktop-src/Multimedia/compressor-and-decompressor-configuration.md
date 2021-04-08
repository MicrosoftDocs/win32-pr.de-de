---
title: Konfiguration des Kompressors und dekompressors
description: Konfiguration des Kompressors und dekompressors
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Videokomprimierungs-Manager (VCM), Konfigurieren von Kompressoren
- VCM (Videokomprimierungs-Manager), Konfigurieren von Kompressoren
- ICM_CONFIGURE Meldung
- Icqueryconfigure-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947642"
---
# <a name="compressor-and-decompressor-configuration"></a>Konfiguration des Kompressors und dekompressors

Die Anwendung kann den Kompressor oder die Debug-Konfiguration automatisch konfigurieren oder die Konfiguration durch den Benutzer zulassen. Wenn dies praktikabel ist, gestatten Sie dem Benutzer die Konfiguration des Kompressors oder der Debug-Konfiguration. Dies gibt Ihnen die Möglichkeit, alle Optionen für den-Kompressor oder-Dekompressor zu berücksichtigen.

Der Benutzer kann den Kompressor oder Dekompressor mithilfe eines Konfigurations Dialogfelds konfigurieren. Sie können die [**ICM \_ configure**](icm-configure.md) -Nachricht an VCM senden (oder das [**icqueryconfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) -Makro verwenden), um zu bestimmen, ob ein Kompressor oder Dekompressor ein Konfigurations Dialogfeld anzeigen kann. Wenn dies der Fall ist, senden Sie die ICM- \_ Konfigurations Nachricht (oder verwenden Sie das [**icconfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) -Makro), um Sie anzuzeigen.

Die Anwendung kann die [**ICM \_ GetState**](icm-getstate.md) -und [**ICM \_ SetState**](icm-setstate.md) -Meldungen senden (oder die Makros [**icgetstatesize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**icgetstate**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)und [**icsetstate**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) verwenden), um den Status für einen Kompressor oder Dekompressor zu erhalten und festzulegen. Wenn die Anwendung den Status erstellt oder ändert, muss Sie vor dem Wiederherstellen des Status das Layout der Daten des Kompressors oder dekompressors abrufen. Wenn Ihre Anwendung den Status von einem Kompressor oder Dekompressor erhält und Sie zum Wiederherstellen des Status in einer nachfolgenden Sitzung verwendet, muss sichergestellt werden, dass nur die Statusinformationen wieder hergestellt werden, die vom verwendeten Kompressor oder Dekompressor abgerufen wurden.

 

 




