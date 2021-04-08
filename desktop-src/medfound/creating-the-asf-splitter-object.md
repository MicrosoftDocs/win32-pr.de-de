---
description: Erstellen des ASF-Splitter Objekts
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Erstellen des ASF-Splitter Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861812"
---
# <a name="creating-the-asf-splitter-object"></a>Erstellen des ASF-Splitter Objekts

Das ASF- *Splitter* Objekt ist ein wmcontainer-Ebenenobjekt, das das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert. Um eine neue Instanz des ASF-Splitter Objekts zu erstellen, rufen Sie die [**mfkreateasfsplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) -Funktion auf. Diese Funktion gibt einen Zeiger auf die [**imfasfsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle zurück, die ein leeres Splitter Objekt darstellt.

Bevor der Splitter die Verarbeitung beginnen kann, muss die Anwendung den Splitter mit Informationen aus dem ASF-Header Objekt initialisieren. Um den Splitter zu initialisieren, nennen Sie die [**imfasfsplitter:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) -Methode. Diese Methode nimmt einen Zeiger auf das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " an, das Header Informationen der zu debuggende ASF-Datei enthält. Die Anwendung muss das ContentInfo-Objekt initialisieren, bevor es an den Splitter übergeben wird, damit die Merkmale der Mediendatei der Anwendung bekannt sind. Die **Initialize** -Methode des Splitters extrahiert streaminginformationen aus dem ContentInfo-Objekt, z. b. streamnummern, sodass der Splitter die Datenpakete analysieren kann.

### <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie ein Splitter erstellt und mit einem vorhandenen ContentInfo-Objekt initialisiert wird.


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
> In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> </dl>

 

 



