---
title: Plug-In-Wrapperfunktionen
description: Wrapperfunktionen, mit denen Sie eine öffentliche Funktion auf jedem Adapter aufrufen können, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu erhalten.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows Biometric Framework API Windows Biometric Framework API , Plug-In-Wrapperfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b3f6991d0723f284bb95ecfd40d7931c48aa8647fb52e2b34a959791a7338b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101250"
---
# <a name="plug-in-wrapper-functions"></a>Plug-In-Wrapperfunktionen

Die Windows Biometric Framework-API enthält Wrapperfunktionen, mit denen Sie eine öffentliche Funktion auf jedem Adapter aufrufen können, der an die Pipeline angefügt ist, ohne manuell einen Zeiger auf den Adapter zu erhalten. Jeder Wrapper überprüft die Eingabeargumente, ruft einen Adapterzeiger ab und ruft die angeforderte Funktion auf. Der **WbioEngineSetHashAlgorithm-Wrapper** verfügt beispielsweise über die folgende Signatur.


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



Die Funktion überprüft, ob das *Pipeline-Argument* nicht **NULL** ist, ob ein Engine-Adapter vorhanden ist und dass die [**EngineAdapterSetHashAlgorithm-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) vorhanden ist. Alle Wrapperfunktionen werden in der Headerdatei Winbio \_ adapter.h definiert. In den folgenden Themen werden die verfügbaren Wrapper behandelt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Wrapper des Engine-Adapters](engine-adapter-wrappers.md)<br/>   | Funktionen, die Sie zum Aufrufen von Funktionen auf dem Engine-Adapter verwenden können. Diese Funktionen werden in Winbio \_ adapter.h definiert.<br/>  |
| [Wrapper für Sensoradapter](sensor-adapter-wrappers.md)<br/>   | Funktionen, die Sie verwenden können, um Funktionen auf Ihrem Sensoradapter aufzurufen. Diese Funktionen werden in Winbio \_ adapter.h definiert.<br/>  |
| [Storage Adapterwrapper](storage-adapter-wrappers.md)<br/> | Funktionen, mit denen Sie Funktionen auf Ihrem Speicheradapter aufrufen können. Diese Funktionen werden in Winbio \_ adapter.h definiert.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-In-Referenz](plug-in-reference.md)
</dt> </dl>

 

 





