---
description: Erstellen des ASF-Splitterobjekts
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Erstellen des ASF-Splitterobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5782f42b53607943704836c350b76e69d872e8d9654959d4453d8e029c21f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600810"
---
# <a name="creating-the-asf-splitter-object"></a>Erstellen des ASF-Splitterobjekts

Das *ASF-Splitterobjekt* ist ein WMContainer-Ebenenobjekt, das das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert. Um eine neue Instanz des ASF-Splitterobjekts zu erstellen, rufen Sie die [**MFCreateASFSplitter-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) auf. Diese Funktion gibt einen Zeiger auf die [**IMFASFSplitter-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) zurück, die ein leeres Splitterobjekt darstellt.

Bevor der Splitter mit der Analyse beginnen kann, muss die Anwendung den Splitter mit Informationen aus dem ASF-Headerobjekt initialisieren. Rufen Sie zum Initialisieren des Splitters die [**IMFASFSplitter::Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) auf. Diese Methode verwendet einen Zeiger auf das [ASF ContentInfo-Objekt,](asf-contentinfo-object.md) das Headerinformationen der zu analysierende ASF-Datei enthält. Die Anwendung muss das ContentInfo-Objekt initialisieren, bevor es an den Splitter übergeben wird, damit die Merkmale der Mediendatei der Anwendung bekannt sind. Die **Initialize-Methode** des Splitters extrahiert Streaminformationen aus dem ContentInfo-Objekt, z. B. Datenstromnummern, damit der Splitter die Datenpakete analysieren kann.

### <a name="example"></a>Beispiel

Das folgende Codebeispiel zeigt, wie Sie einen Splitter erstellen und mit einem vorhandenen ContentInfo-Objekt initialisieren.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> In diesem Beispiel wird die [SafeRelease-Funktion](saferelease.md) verwendet, um Schnittstellenzeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> </dl>

 

 



