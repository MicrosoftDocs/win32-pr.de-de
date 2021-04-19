---
description: Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106362813"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Abschnitt wird beschrieben, wie Sie Windows Media – basierten Inhalt in einer [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) -Anwendung (de) verwenden. Es gibt zwei Haupt Szenarien:

-   Quell Clips. Ein des-Projekts kann Audiodateien und Videoclips aus Windows Media-Dateien enthalten.
-   Das Zielformat. Windows Media ist ein ideales Format für die endgültige Ausgabe eines Video Bearbeitungs Projekts.

Die Anwendung muss ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird, um mit Windows Media-Dateien zu arbeiten. Hierzu wird ein Schlüssel Anbieter Objekt implementiert. Der Schlüssel Anbieter ist ein COM-Objekt, das die **IServiceProvider** -Schnittstelle verfügbar macht. Weitere Informationen zum Implementieren des Schlüssel Anbieters finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.

Zum Verwenden von des mit Windows Media-Dateien ist für die folgenden des-Objekte der Software Schlüssel erforderlich:

-   Die Renderingengine für die Vorschau oder das Schreiben von Dateien.
-   Das mediadet-Objekt, um Video Frames oder Medientypen aus ASF-Dateien zu erhalten.
-   \[! Wichtig\]  
    > Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien. Verwenden Sie immer die einfache Renderengine (CLSID- \_ Renderengine).

     

Um einem Objekt den Software Schlüssel zu übergeben, Fragen Sie das Objekt nach der **IObjectWithSite** -Schnittstelle ab, und nennen Sie **IObjectWithSite:: SetSite** mit einem Zeiger auf Ihren Schlüssel Anbieter. Der folgende Code stellt z. b. den Software Schlüssel für die Renderingengine bereit:


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Um Windows Media-Quell Clips in einem des-Projekt zu verwenden, müssen Sie einfach **IObjectWithSite:: SetSite** für die Renderengine mit einem Zeiger auf Ihren Schlüssel Anbieter aufrufen.

Weitere Informationen zum Schreiben von Windows-Mediendateien finden Sie unter [Schreiben einer Windows Media-Datei in des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



