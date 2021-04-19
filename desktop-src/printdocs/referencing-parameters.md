---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Verweis Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370362"
---
# <a name="referencing-parameters"></a>Verweis Parameter

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Ein konkretes Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße. Beachten Sie, dass Sie auf zwei Parameter verweist: pagemediasizemediasizewidth und pagemediasizemediasizeheight. Jede ParameterRef-Instanz verweist auf eine ParameterDef-Instanz, die an anderer Stelle im printfunktionalitäten-Dokument definiert ist. Weitere Informationen zum ParameterDef-Element finden Sie unter [ParameterDef](parameterdef.md). Konzeptionelle Informationen zum Definieren von Parametern finden Sie unter [ParameterDef-und parameterinit-Elemente](parameterdef-and-parameterinit-elements.md).

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

Das Erstellen einer parametrisierten Option ist nicht ausreichend, um sicherzustellen, dass die Option ordnungsgemäß behandelt und verarbeitet wird. Der printfunktionalitäten/PrintTicket-Anbieter und die Clients müssen zusätzliche Unterstützung für die ordnungsgemäße Implementierung parametrisierter Options Instanzen bereitstellen. Die erforderlichen Verhalten werden in den folgenden Abschnitten beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



