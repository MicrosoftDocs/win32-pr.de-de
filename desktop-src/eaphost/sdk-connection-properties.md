---
title: SDK-Verbindungs Eigenschaften
description: Erfahren Sie mehr über die SDK-Verbindungs Eigenschaften. Sehen Sie sich ein Beispiel an, das eine Instanz des nativen eaphostconfig-Schemas ist.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbd404246055a3c94daff4c029a94f16adfe51b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734600"
---
# <a name="sdk-connection-properties"></a>SDK-Verbindungs Eigenschaften

Bei diesem Beispiel handelt es sich um eine Instanz des nativen [eaphostconfig](eaphostconfigschema-schema.md) -Schemas.

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod>
    <Config>
      <EapType>40</EapType> 
      <ConfigData>seatac.bingo.com</ConfigData> 
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungs Eigenschaften](connection-profiles.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> </dl>

 

 




