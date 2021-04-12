---
description: Die xapo-API stellt die ixapo-Schnittstelle und die cxapobase-Klasse zum Entwickeln neuer xapo-Typen bereit.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: "So wird's gemacht: Erstellen eines XAPOs"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218560"
---
# <a name="how-to-create-an-xapo"></a>So wird's gemacht: Erstellen eines XAPOs

Die xapo-API stellt die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle und die [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse zum Entwickeln neuer xapo-Typen bereit. Die **ixapo** -Schnittstelle enthält alle Methoden, die implementiert werden müssen, um eine neue xapo-Datei zu erstellen. Die **cxapobase** -Klasse stellt eine grundlegende Implementierung der **ixapo** -Schnittstelle bereit. **Cxapobase** implementiert alle **ixapo** -Schnittstellen Methoden außer der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode, die für jedes xapo eindeutig ist.

## <a name="to-create-a-new-static-xapo"></a>So erstellen Sie ein neues statisches xapo

1.  Leiten Sie eine neue xapo-Klasse von der [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Basisklasse ab.

    > [!Note]  
    > Xapos implementiert die **IUnknown** -Schnittstelle. Die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -und [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstellen enthalten die drei **IUnknown** -Methoden: **QueryInterface**, **adressf** und **Release**. [**Cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) stellt Implementierungen aller drei **IUnknown** -Methoden bereit. Eine neue Instanz von **cxapobase** erhält einen Verweis Zähler von 1. Er wird zerstört, wenn der Verweis Zähler 0 (null) ist. Um zuzulassen, dass XAudio2 eine Instanz von xapo zerstört, wenn Sie nicht mehr benötigt wird, nennen Sie **IUnknown:: Release** auf dem xapo, nachdem es einer XAudio2-Wirkungskette hinzugefügt wurde. Weitere Informationen zur Verwendung von xapo mit XAudio2 finden Sie unter Gewusst [wie: Verwenden von xapo in XAudio2](how-to--use-an-xapo-in-xaudio2.md) .

     

2.  Überschreiben Sie die Implementierung der [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse der [**ixapo:: lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -Methode.

    Durch das Überschreiben von [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) können Informationen über das Format der Audiodaten für die Verwendung in [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)gespeichert werden.

3.  Implementieren Sie die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode.

    XAudio2 Ruft die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode auf, wenn ein xapo Audiodaten verarbeiten muss. Der **Prozess** enthält den Großteil des Codes für ein xapo.

## <a name="implementing-the-process-method"></a>Implementieren der Process-Methode

Die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode akzeptiert Streampuffer für Eingabe-und ausgabeaudiodaten. Ein typisches xapo-Objekt erwartet einen Eingabestreampuffer und einen ausgabestreampuffer. Sie sollten die Verarbeitung von Daten aus dem Eingabestreampuffer auf das in der [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -Funktion angegebene Format und alle Flags, die an die **Prozess** Funktion mit dem Eingabestreampuffer weitergegeben wurden, basieren. Kopieren Sie die verarbeiteten Eingabedaten Strom-Puffer Daten in den ausgabestreampuffer. Legen Sie den bufferflags-Parameter des ausgabestreampuffers entweder als [**\_ \_ gültiger xapo-Puffer**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) oder **xapo- \_ \_ Puffer** unbeaufsichtigt fest

Im folgenden Beispiel wird eine [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -und [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Implementierung veranschaulicht, mit der Daten einfach aus einem Eingabepuffer in einen Ausgabepuffer kopiert werden. Es gibt jedoch keine Verarbeitung, wenn der Eingabepuffer mit dem automatischen [**xapo \_ - \_ Puffer**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags)markiert ist.


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



Beim Schreiben einer [**Prozess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) Methode ist es wichtig zu beachten, dass sich XAudio2 Audiodaten überlappen. Dies bedeutet, dass die Daten aus den einzelnen Kanälen für eine bestimmte Stichproben Nummer nebeneinander liegen. Wenn z. b. eine 4-Kanal-Welle in einer XAudio2 Source-Sprache vorhanden ist, sind die Audiodaten ein Beispiel für Channel 0, ein Beispiel für Channel 1, ein Beispiel für Channel 2, ein Beispiel für Channel 3 und anschließend das nächste Beispiel der Kanäle 0, 1, 2, 3 usw.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[Übersicht über xapo](xapo-overview.md)
</dt> </dl>

 

 
