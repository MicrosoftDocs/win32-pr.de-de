---
description: Wichtige Funktionen für das Debuggen von Abschnitten
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Wichtige Funktionen für das Debuggen von Abschnitten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65834d84900ad3ac893cb75493a59902629fec15523cfaca8974a6684ba9c409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908070"
---
# <a name="critical-section-debugging-functions"></a>Wichtige Funktionen für das Debuggen von Abschnitten

Diese Funktionen helfen beim Debuggen kritischer Abschnitte im Code, wodurch die Ursache eines Deadlocks leichter gefunden werden kann. Diese Funktionen verwenden die [**CCritSec-Hilfsklasse.**](ccritsec.md)



| Funktion                             | BESCHREIBUNG                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Gibt **TRUE zurück,** wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt.  |
| [**CritCheckOut**](critcheckout.md) | Gibt **FALSE zurück,** wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt. |
| [**DbgLockTrace**](dbglocktrace.md) | Aktiviert oder deaktiviert die Debugprotokollierung für einen bestimmten kritischen Abschnitt.              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Hilfsprogrammen](debugging-utilities.md)
</dt> </dl>

 

 



