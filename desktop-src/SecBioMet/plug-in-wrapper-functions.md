---
title: Plug-in-Wrapper Funktionen
description: Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem Adapter aufzurufen, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu beschaffen.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API-Windows-Biometrieframework API (Windows-Biometrieframework API), Plug-in-Wrapper Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856711"
---
# <a name="plug-in-wrapper-functions"></a>Plug-in-Wrapper Funktionen

Die Windows-Biometrieframework-API umfasst Wrapper Funktionen, die es Ihnen ermöglichen, eine öffentliche Funktion auf jedem an die Pipeline angefügten Adapter aufzurufen, ohne manuell einen Zeiger auf den Adapter zu beschaffen. Jeder Wrapper überprüft die Eingabeargumente, Ruft einen Adapter Zeiger ab und ruft die angeforderte Funktion auf. Der **wbioenginesethashalgorithm** -Wrapper hat z. b. die folgende Signatur.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



Die Funktion überprüft, ob das *Pipeline* Argument nicht **null** ist, dass ein Engine-Adapter vorhanden ist, und dass die [**engineadaptersethashalgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) -Funktion vorhanden ist. Alle Wrapper Funktionen sind in der Header Datei "winbio \_ Adapter. h" definiert. In den folgenden Themen werden die verfügbaren Wrapper erläutert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Engine-Adapter Wrapper](engine-adapter-wrappers.md)<br/>   | Funktionen, die Sie verwenden können, um Funktionen für den Engine-Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.<br/>  |
| [Sensor Adapter-Wrapper](sensor-adapter-wrappers.md)<br/>   | Funktionen, die Sie verwenden können, um Funktionen auf dem Sensor Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.<br/>  |
| [Wrapper für Speicher Adapter](storage-adapter-wrappers.md)<br/> | Funktionen, die Sie verwenden können, um Funktionen auf Ihrem Speicher Adapter aufzurufen. Diese Funktionen sind in winbio \_ Adapter. h definiert.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-in-Referenz](plug-in-reference.md)
</dt> </dl>

 

 





