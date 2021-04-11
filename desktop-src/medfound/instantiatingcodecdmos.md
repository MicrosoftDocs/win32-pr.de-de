---
description: Instanziieren von Codec-DMOS
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Instanziieren von Codec-DMOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958904"
---
# <a name="instantiating-codec-dmos"></a>Instanziieren von Codec-DMOS

Sie können einen Codec-DMO erstellen, indem Sie die com-Funktion [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen. Sie müssen den Klassen Bezeichner des DMO, den Schnittstellen Bezeichner von **imediaobject** und einen Zeiger auf einen **imediaobject** -Zeiger übergeben.

Die Klassen Bezeichner der Codec-DMOS werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert.

Die Konstante für den **imediaobject** -Schnittstellen Bezeichner ist IID \_ imediaobject.

Im folgenden Codebeispiel wird veranschaulicht, wie eine Instanz eines Codec-DMO erstellt wird:


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

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
