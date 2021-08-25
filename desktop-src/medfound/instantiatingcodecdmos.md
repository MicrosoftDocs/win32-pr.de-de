---
description: Instanziieren von Codec-DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Instanziieren von Codec-DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957550"
---
# <a name="instantiating-codec-dmos"></a>Instanziieren von Codec-DMOs

Sie können einen Codec DMO erstellen, indem Sie die [**COM-Funktion CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen. Sie müssen den Klassenbezeichner des DMO, den Schnittstellenbezeichner von **IMediaObject** und einen Zeiger auf einen **IMediaObject-Zeiger** übergeben.

Die Klassenbezeichner der Codec-DMOs werden in der Headerdatei wmcodecdsp.h als Konstanten definiert.

Die Konstante für den **IMediaObject-Schnittstellenbezeichner** ist IID \_ IMediaObject.

Im folgenden Codebeispiel wird veranschaulicht, wie eine Instanz eines Codecs DMO erstellt wird:


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
