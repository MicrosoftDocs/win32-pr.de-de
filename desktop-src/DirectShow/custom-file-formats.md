---
description: Benutzerdefinierte Dateiformate
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Benutzerdefinierte Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a478e7818701008c31d1d0c5a6e4924540ed818be19f7b50fe3ed278aa6f3ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998690"
---
# <a name="custom-file-formats"></a>Benutzerdefinierte Dateiformate

Wenn Sie über einen benutzerdefinierten Mux- oder Dateiwriterfilter verfügen, der Ihr eigenes Dateiformat unterstützt, können Sie die CLSID als ersten Parameter der [**ICaptureGraphBuilder2::SetOutputFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) angeben:


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Weitere Informationen zu dieser Verwendung finden Sie unter [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



