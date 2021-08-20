---
title: Verwalten von Datenblöcken durch Abfragen
description: Verwalten von Datenblöcken durch Abfragen
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- Waveformaudio, Abfragen von Datenblöcken
- Audiodatenblöcke,Abruf
- Abfragen von Audiodatenblöcken
- WAVEHDR-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c84e75eccaf34ef16ccadefb4dae42931854a0c6c4278003fb5c01b0c551f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139166"
---
# <a name="managing-data-blocks-by-polling"></a>Verwalten von Datenblöcken durch Abfragen

Zusätzlich zur Verwendung einer Rückruffunktion können Sie den **dwFlags-Member** einer [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) abfragen, um zu bestimmen, wann ein Audiogerät mit einem Datenblock fertig ist. Manchmal ist es besser, **dwFlags** abzufragen, als auf einen anderen Mechanismus zum Empfangen von Nachrichten von den Treibern zu warten. Nachdem Sie beispielsweise die [**waveOutReset-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) aufgerufen haben, um ausstehende Datenblöcke freizugeben, können Sie sofort abfragen, um sicherzustellen, dass die Datenblöcke freigegeben wurden, bevor [**Sie waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) aufrufen und den Arbeitsspeicher für den Datenblock freigeben.

Sie können das Flag WHDR \_ DONE verwenden, um den **dwFlags-Member** zu testen. Sobald das Flag WHDR \_ DONE im **dwFlags-Member** der **WAVEHDR-Struktur** festgelegt ist, ist der Treiber mit dem Datenblock fertig.

 

 