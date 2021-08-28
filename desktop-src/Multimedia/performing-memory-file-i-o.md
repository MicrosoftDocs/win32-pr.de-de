---
title: Ausführen von Speicherdatei-E/A
description: Ausführen von Speicherdatei-E/A
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- Multimediadatei-E/A, Arbeitsspeicher
- Datei-E/A, Arbeitsspeicher
- Eingabe und Ausgabe (E/A), Arbeitsspeicher
- E/A (Eingabe und Ausgabe), Arbeitsspeicher
- Speicher-E/A
- mmioOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a2b1e2e47ffccc21b2684dcb6bd285b7e55470776fb57eb382a969091a19e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805890"
---
# <a name="performing-memory-file-io"></a>Ausführen von Speicherdatei-E/A

Mit den E/A-Diensten für Multimediadateien können Sie einen Speicherblock als Datei behandeln. Dies kann nützlich sein, wenn Sie bereits über ein Dateiimage im Arbeitsspeicher verfügen. Mit Speicherdateien können Sie die Anzahl von Sonderbedingungen im Code reduzieren, da Sie für E/A-Zwecke Speicherdateien so behandeln können, als ob es sich um datenträgerbasierte Dateien wäre. Sie können auch Speicherdateien mit der Zwischenablage verwenden.

Wie bei E/A-Puffern können Speicherdateien Arbeitsspeicher verwenden, der von der Anwendung oder vom Datei-E/A-Manager zugeordnet wird. Darüber hinaus können Speicherdateien entweder erweiterbar oder nicht erweiterbar sein. Wenn der Datei-E/A-Manager das Ende einer erweiterbaren Speicherdatei erreicht, wird die Speicherdatei um ein vordefiniertes Inkrement erweitert.

Um eine Speicherdatei zu öffnen, verwenden Sie die [**mmioOpen-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) bei der der *szFilename-Parameter* auf **NULL** und das MMIO READWRITE-Flag im \_ *dwOpenFlags-Parameter festgelegt* ist. Legen Sie *den lpmmioinfo-Parameter* so fest, dass er auf eine [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) zeigen soll, die wie folgt eingerichtet wurde:

1.  Legen Sie den **pIOProc-Member** auf **NULL fest.**
2.  Legen Sie **das fccIOProc-Mitglied** auf FOURCC \_ MEM fest.
3.  Legen Sie den **pchBuffer-Member** so fest, dass er auf den Speicherblock zeigen soll. Wenn Sie anfordern, dass der Datei-E/A-Manager den Speicherblock zuordnt, legen **Sie pchBuffer** auf **NULL fest.**
4.  Legen Sie **den cchBuffer-Member** auf die Anfangsgröße des Speicherblocks fest.
5.  Legen Sie **den AdwInfo-Member** auf die minimale Erweiterungsgröße des Speicherblocks fest. Legen Sie für eine nicht ersetzbare Speicherdatei **adwInfo** auf **NULL fest.**
6.  Legen Sie alle anderen Member auf 0 (null) fest.

Es gibt keine Einschränkungen bei der Zuweisung von Arbeitsspeicher für die Verwendung als nicht ersetzbare Speicherdatei.

 

 