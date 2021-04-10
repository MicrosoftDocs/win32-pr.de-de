---
title: Erstellen eines Riff Segments
description: Erstellen eines Riff Segments
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- Multimedia-Datei-e/a, Erstellen von Riff Segmenten
- Datei-e/a, Erstellen eines Riff Segments
- Eingabe und Ausgabe (e/a), Erstellen eines Riff Blocks
- E/a (Eingabe und Ausgabe), Erstellen eines Riff Blocks
- Erstellen eines Riff Segments
- mmiokreatechunk-Funktion
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858205"
---
# <a name="creating-a-riff-chunk"></a>Erstellen eines Riff Segments

Im folgenden Beispiel wird die [**mmiokreatechunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) -Funktion verwendet, um einen Block mit dem Block Bezeichner "Riff" und dem Formulartyp "rdib" zu erstellen.


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Wenn Sie einen "Riff"-oder "List"-Block erstellen, müssen Sie den Formulartyp oder den Listentyp im **fcctype** -Member der [**mmckinfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) -Struktur angeben. Im vorherigen Beispiel ist "rdib" der Formulartyp.

Wenn Sie die Größe des Daten Felds in einem neuen Block kennen, können Sie den **cksize** -Member der **mmckinfo** -Struktur festlegen, wenn Sie den Block erstellen. Dieser Wert wird in das Feld Datengröße im neuen Block geschrieben. Wenn dieser Wert nicht korrekt ist, wenn Sie [**mmioascend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) zum Markieren des Blocks enden, wird er automatisch umgeschrieben, um die korrekte Größe des Daten Felds widerzuspiegeln.

Nachdem Sie mithilfe der [**mmiokreatechunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) -Funktion einen Block erstellt haben, wird die Dateiposition auf das Datenfeld des Blocks (8 Bytes vom Anfang des Blocks) festgelegt. Wenn es sich bei dem Block um einen "Riff"-oder "List"-Block handelt, wird die Dateiposition auf den Speicherort festgelegt, der dem Typ oder dem Auflistungstyp folgt (12 Bytes vom Anfang des Blocks).

 

 