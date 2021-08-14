---
title: Überwachen des Fortschritts von Ausstellern und Dekomprimierern
description: Überwachen des Fortschritts von Ausstellern und Dekomprimierern
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Videokomprimierungs-Manager (VCM), Überwachung
- VCM (Videokomprimierungs-Manager),Überwachung
- ICSetStatusProc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44707cb6a8fbdb19b1d71fed6c71498b51936b9d089354277c6767586b4b8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373499"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Überwachen des Fortschritts von Ausstellern und Dekomprimierern

Ihre Anwendung kann den Fortschritt eines längeren Vorgangs überwachen, der von einem Sprech- oder Dekomprimierer ausgeführt wird, indem sie die Adresse einer Rückruffunktion sendet. Sie können die [**ICSetStatusProc-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) verwenden, um die Adresse an den Entpacker oder Dekomprimierer zu senden. Wenn der Entpacker oder Dekomprimierer diese Adresse empfängt, sendet er Statusmeldungen an die Funktion. Diese Meldungen geben an, ob der Vorgang gestartet, beendet, ergibt oder fortgesetzt wird.

 

 




