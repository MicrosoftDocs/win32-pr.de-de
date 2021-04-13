---
title: Ausführen von Speicherdatei-e/a
description: Ausführen von Speicherdatei-e/a
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- Multimedia-Datei-e/a, Arbeitsspeicher
- Datei-e/a, Arbeitsspeicher
- Eingabe und Ausgabe (e/a), Arbeitsspeicher
- E/a (Eingabe und Ausgabe), Arbeitsspeicher
- Arbeitsspeicher-e/a
- mmioopen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472749"
---
# <a name="performing-memory-file-io"></a>Ausführen von Speicherdatei-e/a

Die Multimedia-Datei-e/a-Dienste ermöglichen es Ihnen, einen Speicherblock als Datei zu behandeln. Dies kann hilfreich sein, wenn Sie bereits über ein Datei Image im Arbeitsspeicher verfügen. Mithilfe von Speicherdateien können Sie die Anzahl von Sonderbedingungen im Code reduzieren, da Sie für e/a-Zwecke Speicherdateien als Datenträger basierte Dateien behandeln können. Sie können auch Speicherdateien mit der Zwischenablage verwenden.

Wie bei e/a-Puffern können Speicherdateien den von der Anwendung oder dem Datei-e/a-Manager zugeordneten Arbeitsspeicher verwenden. Außerdem können Speicherdateien entweder erweiterbar oder nicht erweiterbar sein. Wenn der Datei-e/a-Manager das Ende einer erweiterbaren Speicherdatei erreicht, erweitert er die Speicherdatei um ein vordefiniertes Inkrement.

Um eine Speicherdatei zu öffnen, verwenden Sie die [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion, wobei der *szFilename* -Parameter auf **null** festgelegt ist und das MMIO- \_ Schreib Flag im *dwOpenFlags* -Parameter festgelegt ist. Legen Sie den *lpmmioinfo* -Parameter so fest, dass er auf eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur verweist, die wie folgt eingerichtet wurde:

1.  Legen Sie den **pioproc** -Member auf **null** fest.
2.  Legen Sie den **fccioproc** -Member auf FourCC \_ mem fest.
3.  Legen Sie den **pchBuffer** -Member so fest, dass er auf den Speicherblock verweist. Legen Sie **pchBuffer** auf **null** fest, um anzufordern, dass der Datei-e/a-Manager den Speicherblock zuweist.
4.  Legen Sie den **cchBuffer** -Member auf die anfängliche Größe des Speicherblocks fest.
5.  Legen Sie den **adwinfo** -Member auf die minimale Erweiterungs Größe des Speicherblocks fest. Legen Sie für eine nicht erweiterbare Speicherdatei **adwinfo** auf **null** fest.
6.  Legen Sie alle anderen Elemente auf 0 (null) fest.

Es gibt keine Einschränkungen für das belegen von Speicher für die Verwendung als nicht erweiterbare Speicherdatei.

 

 