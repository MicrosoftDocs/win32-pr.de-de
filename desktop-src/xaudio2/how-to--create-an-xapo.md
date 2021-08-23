---
description: Die XAPO-API stellt die IXAPO-Schnittstelle und die CXAPOBase-Klasse zum Erstellen neuer XAPO-Typen bereit.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: "So wird's gemacht: Erstellen eines XAPOs"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17729c5a6d872d98443c85f79dc72e8eee6dd2233b99f31e189a9eb28708e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583850"
---
# <a name="how-to-create-an-xapo"></a>So wird's gemacht: Erstellen eines XAPOs

Die XAPO-API stellt die [**IXAPO-Schnittstelle**](/windows/desktop/api/XAPO/nn-xapo-ixapo) und die [**CXAPOBase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) zum Erstellen neuer XAPO-Typen bereit. Die **IXAPO-Schnittstelle** enthält alle Methoden, die implementiert werden müssen, um eine neue XAPO zu erstellen. Die **CXAPOBase-Klasse** stellt eine grundlegende Implementierung der **IXAPO-Schnittstelle** bereit. **CXAPOBase** implementiert alle **IXAPO-Schnittstellenmethoden** mit Ausnahme der [**IXAPO::P rocess-Methode,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) die für jedes XAPO eindeutig ist.

## <a name="to-create-a-new-static-xapo"></a>So erstellen Sie ein neues statisches XAPO

1.  Leiten Sie eine neue XAPO-Klasse von der [**CXAPOBase-Basisklasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) ab.

    > [!Note]  
    > XAPOs implementieren die **IUnknown-Schnittstelle.** Die [**Schnittstellen IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) und [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) enthalten die drei **IUnknown-Methoden:** **QueryInterface,** **AddRef** und **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) stellt Implementierungen aller drei **IUnknown-Methoden** bereit. Eine neue Instanz von **CXAPOBase** hat einen Verweiszähler von 1. Er wird zerstört, wenn der Verweiszähler 0 wird. Damit XAudio2 eine Instanz einer XAPO zerstören kann, wenn sie nicht mehr benötigt wird, rufen **Sie IUnknown::Release** für die XAPO auf, nachdem sie einer XAudio2-Effektkette hinzugefügt wurde. Weitere Informationen zur Verwendung [eines XAPO mit XAudio2](how-to--use-an-xapo-in-xaudio2.md) finden Sie unter Vorgehensweise: Verwenden eines XAPO in XAudio2.

     

2.  Überschreiben Sie die [**CXAPOBase-Klassenimplementierung**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) der [**IXAPO::LockForProcess-Methode.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)

    Durch das Überschreiben von [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) können Informationen über das Format von Audiodaten zur Verwendung in [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)gespeichert werden.

3.  Implementieren Sie die [**IXAPO::P rocess-Methode.**](/windows/win32/api/xapo/nf-xapo-ixapo-process)

    XAudio2 ruft die [**IXAPO::P rocess-Methode**](/windows/win32/api/xapo/nf-xapo-ixapo-process) auf, wenn ein XAPO Audiodaten verarbeiten muss. **Der Prozess** enthält den Großteil des Codes für eine XAPO.

## <a name="implementing-the-process-method"></a>Implementieren der Prozessmethode

Die [**IXAPO::P rocess-Methode**](/windows/win32/api/xapo/nf-xapo-ixapo-process) akzeptiert Streampuffer für Eingabe- und Ausgabeaudiodaten. Ein typischer XAPO-Typ erwartet einen Eingabestreampuffer und einen Ausgabestreampuffer. Sie sollten die Verarbeitung von Daten aus dem Eingabedatenstrompuffer auf dem in der [**LockForProcess-Funktion**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) angegebenen Format und allen an die **Process-Funktion** übergebenen Flags mit dem Eingabestreampuffer basieren. Kopieren Sie die verarbeiteten Eingabestreampufferdaten in den Ausgabestreampuffer. Legen Sie den BufferFlags-Parameter des Ausgabestreampuffers entweder auf [**XAPO \_ BUFFER \_ VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) oder **XAPO \_ BUFFER \_ SILENT** fest.

Im folgenden Beispiel wird eine [**LockForProcess-**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) und [**Process-Implementierung**](/windows/win32/api/xapo/nf-xapo-ixapo-process) veranschaulicht, die einfach Daten aus einem Eingabepuffer in einen Ausgabepuffer kopiert. Es erfolgt jedoch keine Verarbeitung, wenn der Eingabepuffer mit [**XAPO \_ BUFFER \_ SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags)markiert ist.


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



Beim Schreiben einer [**Process-Methode**](/windows/win32/api/xapo/nf-xapo-ixapo-process) ist es wichtig zu beachten, dass XAudio2-Audiodaten verschachtelt sind. Dies bedeutet, dass daten aus jedem Kanal für eine bestimmte Beispielnummer angrenzen. Wenn beispielsweise eine 4-Kanal-Welle in einer XAudio2-Quellstimme wiedergegeben wird, sind die Audiodaten ein Beispiel für Kanal 0, ein Beispiel für Kanal 1, ein Beispiel für Kanal 2, ein Beispiel für Kanal 3 und dann das nächste Beispiel der Kanäle 0, 1, 2, 3 usw.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[Übersicht über XAPO](xapo-overview.md)
</dt> </dl>

 

 
