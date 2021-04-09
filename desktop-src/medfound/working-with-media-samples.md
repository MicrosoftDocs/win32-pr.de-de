---
description: Arbeiten mit Medien Beispielen
ms.assetid: 10b547b1-6624-4d49-9852-a5fff4eb70e7
title: Arbeiten mit Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a31fa8ff17c2dabcac9d110b530751d22fdf7b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961104"
---
# <a name="working-with-media-samples"></a>Arbeiten mit Medien Beispielen

In diesem Thema wird beschrieben, wie Sie die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle zum Bearbeiten von Medien Beispiel Objekten verwenden. Eine allgemeine Übersicht über die Medien Beispiele finden Sie unter [Medien Beispiele](media-samples.md).

Um ein neues Medien Beispiel zu erstellen, rufen Sie die [**mfkreatesample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) -Funktion auf. Anfänglich ist die Puffer Liste des Beispiels leer. Um einen Puffer am Ende der Liste hinzuzufügen, nennen Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).

Der folgende Code zeigt, wie Sie ein Beispiel erstellen und diesem einen Puffer hinzufügen.


```C++
HRESULT CreateMediaSample(DWORD cbData, IMFSample **ppSample)
{
    HRESULT hr = S_OK;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    hr = MFCreateSample(&pSample);

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbData, &pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        *ppSample = pSample;
        (*ppSample)->AddRef();
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



Die empfohlene Vorgehensweise zum Abrufen der Puffer aus dem Beispiel besteht darin, [**imfsample:: converttezusammenguousbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer)aufzurufen. Diese Methode gibt einen einzelnen kontinuierlichen Puffer zurück.

Um die Puffer in der Liste zu durchlaufen, rufen Sie zunächst [**imfsample:: getbuffercount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount)auf. Diese Methode gibt die Anzahl von Puffern zurück. Rufen Sie dann [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) auf, und geben Sie den Index des abzurufenden Puffers an. Puffer werden von 0 (null) indiziert.

Der folgende Code zeigt, wie die Puffer in einem Beispiel durchlaufen werden.


```C++
IMFMediaBuffer *pBuffer = NULL;
DWORD cBuffers = 0;

hr = pSample->GetBufferCount(&cBuffers);

if (SUCCEEDED(hr))
{
    for (DWORD i = 0; i < cBuffers; i++)
    {
        hr = pSample->GetBufferByIndex(i, &pBuffer);

        // Use buffer (not shown).

        SafeRelease(&pBuffer);

        if (FAILED(hr))
        {
            break;
        }
    }
}
```



Beispiele haben einen Zeitstempel und eine Dauer. Der Zeitstempel gibt an, wann die Daten im Beispiel relativ zur Präsentationszeit gerendert werden sollen. Die Dauer ist die Zeitspanne, für die die Daten gerendert werden sollen. In der Regel legt die Komponente, die die Daten generiert, den anfänglichen Zeitstempel und die Dauer fest. Diese Werte werden möglicherweise von der Medien Sitzung geändert. Um den Zeitstempel festzulegen, wenden Sie [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)an. Um die Dauer festzulegen, müssen Sie [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)aufrufen.

Beispiele können auch über Attribute verfügen, die zusätzliche Informationen über das Beispiel enthalten. Eine Liste der Beispiel Attribute finden Sie unter [Beispiel Attribute](sample-attributes.md). Zum Festlegen und Abrufen von Attributen verwenden Sie die [**imfattributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) erbt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[Medien Puffer](media-buffers.md)
</dt> </dl>

 

 



