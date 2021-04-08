---
description: In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppieren, sodass Sie gleichzeitig wirksam werden.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: "So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866484"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz

In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppieren, sodass Sie gleichzeitig wirksam werden.

## <a name="to-group-audio-methods-as-an-operation-set"></a>So gruppieren Sie Audiomethoden als Vorgangs Satz

1.  Deklarieren Sie einen globalen Vorgangs Satz-Zählers.

    Der [Vorgangs Satz](operation-sets.md) -Counter stellt sicher, dass jeder Vorgangs Satz eindeutig ist.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Erhöhen Sie den globalen Counter.

    Jedes Mal, wenn Sie einen neuen [Vorgangs Satz](operation-sets.md)übermitteln, sollte der globale gegen Schritt erhöht werden, um sicherzustellen, dass jeder Satz eindeutig ist.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Gruppieren Sie die Methodenaufrufe durch Festlegen der Parameter für den [Vorgangs Satz](operation-sets.md) .

4.  Legen Sie die Parameter des [Vorgangs Satzes](operation-sets.md) auf den aktuellen Wert des globalen Leistungs Zählers fest.

    In diesem Fall werden vier Aufrufe von [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) als ein [Vorgangs Satz](operation-sets.md)gruppiert. Das Gruppieren der Aufrufe bewirkt, dass alle vier Sounds gleichzeitig gestartet werden.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Starten Sie den [Vorgangs Satz](operation-sets.md).

    Nachdem Sie alle Methoden im Satz aufgerufen haben, starten Sie den Satz durch Aufrufen von [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem aktuellen Wert des globalen Leistungs Zählers.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgangs Sätze](operation-sets.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[XAudio2-Vorgangs Sätze](xaudio2-operation-sets.md)
</dt> </dl>

 

 
