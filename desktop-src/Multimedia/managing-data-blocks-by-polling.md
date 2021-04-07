---
title: Verwalten von Datenblöcken durch Abrufen
description: Verwalten von Datenblöcken durch Abrufen
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- Wellenform-Audiodaten, Abrufen von Datenblöcken
- Audiodatenblöcke, Abrufen
- Abrufen von audiodatenblöcken
- Wavehdr-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038851"
---
# <a name="managing-data-blocks-by-polling"></a>Verwalten von Datenblöcken durch Abrufen

Zusätzlich zur Verwendung einer Rückruffunktion können Sie den **dwFlags** -Member einer [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur Abfragen, um zu bestimmen, wann ein Audiogerät mit einem Datenblock fertig ist. Manchmal ist es besser, **dwFlags** abzufragen, als auf einen anderen Mechanismus zum Empfangen von Nachrichten von den Treibern zu warten. Nachdem Sie z. b. die [**waveoutset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion zum Freigeben von ausstehenden Datenblöcken aufgerufen haben, können Sie sofort Abfragen, um sicherzustellen, dass die Datenblöcke freigegeben wurden, bevor Sie [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) aufrufen und den Arbeitsspeicher für den Datenblock freigeben.

Sie können das whdr \_ done-Flag verwenden, um **den dwFlags** -Member zu testen. Sobald das Flag "whdr \_ Done" im **dwFlags** -Member der **wavehdr** -Struktur festgelegt ist, wird der Treiber mit dem Datenblock beendet.

 

 