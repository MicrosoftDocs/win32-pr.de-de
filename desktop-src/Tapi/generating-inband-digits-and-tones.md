---
description: Nachdem sich ein-Rückruf im verbundenen Zustand befindet, kann er über ihn übermittelt werden.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Erstellen von Inband-Ziffern und-Tönen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354446"
---
# <a name="generating-inband-digits-and-tones"></a>Erstellen von Inband-Ziffern und-Tönen

Nachdem sich ein-Rückruf im *verbundenen* Zustand befindet, kann er über ihn übermittelt werden. Es werden zwei Funktionen bereitgestellt, die eine End-to-End-Inband-Signalisierung zwischen der Anwendung und den Remote Stations Geräten ermöglichen, z. b Eine Funktion ist " [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)", die bei einem Anruf inbandziffern generiert und diese über den voicechannel signalisiert. Ziffern können als Zeichen folgen oder als DTMF-Töne signalisiert werden. Die andere Funktion ist " [**linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)", die es der Anwendung ermöglicht, eine Vielzahl von mehr Frequenz Tönen (über den Mediendaten Strom) zu generieren. Dadurch werden telefonietöne, wie z. b. "Ringback", "Beep" und "ausgelastet", sowie beliebige Multifrequenz-, multikad-Töne erzeugt.

Nur eine Ziffern-oder Tongenerierung kann bei einem Aufruf zu einem beliebigen Zeitpunkt ausgeführt werden. Wenn die Ziffern-oder Tongenerierung abgeschlossen ist, wird eine [**Zeile zum \_ Generieren von Zeilen**](line-generate.md) an die Anwendung gesendet, die die Generierung angefordert hat. Wenn mehrere Ziffern generiert werden, wird nur eine einzelne Nachricht zurückgesendet, nachdem alle Ziffern generiert wurden. Beim Aufrufen von [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) oder [**linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) während der Ziffern-oder Tongenerierung wird die Generierung abgebrochen, und die Zeile zum \_ generieren der Nachricht wird an die Anwendung gesendet, deren Generierung mit einer Abbruch Angabe abgebrochen wurde.

 

 



