---
description: Erfahren Sie mehr über das Verweisen auf Parameter und das ParameterDef-Element. Ein Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Verweisen auf Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405323"
---
# <a name="referencing-parameters"></a>Verweisen auf Parameter

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Ein konkretes Beispiel für eine Option, die ein ParameterRef-Element enthält, ist die Option für die benutzerdefinierte Mediengröße. Beachten Sie, dass auf zwei Parameter verwiesen wird: PageMediaSizeMediaSizeWidth und PageMediaSizeMediaSizeHeight. Jede ParameterRef-Instanz verweist auf eine ParameterDef-Instanz, die an anderer Stelle im PrintCapabilities-Dokument definiert ist. Informationen zum ParameterDef-Element finden Sie unter [ParameterDef.](parameterdef.md) Konzeptionelle Informationen zum Definieren von Parametern finden Sie unter [ParameterDef und ParameterInit Elements](parameterdef-and-parameterinit-elements.md).

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

Lediglich das Erstellen einer parametrisierten Option reicht nicht aus, um sicherzustellen, dass die Option ordnungsgemäß behandelt und verarbeitet wird. Der PrintCapabilities/PrintTicket-Anbieter und -Clients müssen zusätzliche Unterstützung bereitstellen, um parametrisierte Optionsinstanzen ordnungsgemäß zu implementieren. Die erforderlichen Verhaltensweisen werden in den folgenden Abschnitten beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



