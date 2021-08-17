---
title: Konfiguration von "Metrik" und "Dekomprimierung"
description: Konfiguration von "Metrik" und "Dekomprimierung"
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Videokomprimierungs-Manager (VCM), Konfigurieren von Patienten
- VCM (Videokomprimierungs-Manager),Konfigurieren von Patienten
- ICM_CONFIGURE Meldung
- ICQueryConfigure-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8905ea35d65fc3eda3ddee130039503d8e26555665aae9efa517cb399349475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144975"
---
# <a name="compressor-and-decompressor-configuration"></a>Konfiguration von "Metrik" und "Dekomprimierung"

Ihre Anwendung kann die Entpackung oder den Dekomprimierer automatisch konfigurieren oder dem Benutzer erlauben, sie zu konfigurieren. Wenn dies praktikabel ist, erlauben Sie es dem Benutzer, den Entpackungs- oder Dekomprimierer zu konfigurieren. dadurch können Sie nicht alle Optionen für die Sprech- oder Dekomprimierung in Betracht ziehen.

Der Benutzer kann die Entpackung oder den Dekomprimierer mithilfe eines Konfigurationsdialogfelds konfigurieren. Sie können die [**ICM \_ CONFIGURE-Nachricht**](icm-configure.md) an den VCM senden (oder das [**ICQueryConfigure-Makro**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) verwenden), um zu bestimmen, ob ein Komprimierungs- oder Dekomprimierer ein Konfigurationsdialogfeld anzeigen kann. Wenn ja, senden Sie die ICM \_ CONFIGURE-Nachricht (oder verwenden Sie das [**ICConfigure-Makro),**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) um sie anzuzeigen.

Ihre Anwendung kann die [**ICM \_ GETSTATE-**](icm-getstate.md) und [**ICM \_ SETSTATE-Nachrichten**](icm-setstate.md) senden (oder die [**IcGetStateSize-,**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize) [**ICGetState-**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)und [**ICSetState-Makros**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) verwenden), um den Status für einen Veralten oder Dekomprimierer abzurufen und festzulegen. Wenn Ihre Anwendung den Status erstellt oder ändert, muss sie das Layout der Druck- oder Dekomprimierungsdaten abrufen, bevor der Status wiederhergestellt wird. Wenn Ihre Anwendung den Status von einem Komprimierungs- oder Dekomprimierer erhält und sie verwendet, um den Status in einer nachfolgenden Sitzung wiederherzustellen, muss sie auch sicherstellen, dass nur Statusinformationen wiederhergestellt werden, die von der aktuell verwendeten Füllung oder dekomprimierung abgerufen wurden.

 

 




