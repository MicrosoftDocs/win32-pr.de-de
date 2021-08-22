---
description: In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppiert werden können, damit sie gleichzeitig wirksam werden.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: "So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f5c1d27e33db4c0f7910761a7be574b72e9ac7aaa91b14329fa003792860d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082924"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a>So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz

In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppiert werden können, damit sie gleichzeitig wirksam werden.

## <a name="to-group-audio-methods-as-an-operation-set"></a>So gruppen Sie Audiomethoden als Vorgangssatz

1.  Deklarieren Sie einen globalen Vorgangssatzzähler.

    Der [Vorgangssatzzähler](operation-sets.md) stellt sicher, dass jeder Vorgangssatz eindeutig ist.

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  Inkrementiert den globalen Zähler.

    Jedes Mal, wenn Sie einen neuen [Vorgangssatz übermitteln,](operation-sets.md)sollte der globale Zähler erhöht werden, um sicherzustellen, dass jeder Satz eindeutig ist.

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  Gruppieren Sie die Methodenaufrufe, indem Sie [ihre Vorgangssatzparameter](operation-sets.md) festlegen.

4.  Legen Sie [die Parameter für den](operation-sets.md) Vorgangssatz auf den aktuellen Wert des globalen Leistungsindikators fest.

    In diesem Fall werden vier Aufrufe von [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) als ein [Vorgangssatz gruppiert.](operation-sets.md) Das Gruppieren der Aufrufe bewirkt, dass alle vier Sounds genau zur gleichen Zeit beginnen.

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  Starten Sie den [Vorgangssatz](operation-sets.md).

    Nachdem Sie alle Methoden in der Menge aufruft, starten Sie den Satz, indem Sie [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem aktuellen Wert des globalen Zählers aufrufen.

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgangssätze](operation-sets.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[XAudio2-Vorgangssätze](xaudio2-operation-sets.md)
</dt> </dl>

 

 
