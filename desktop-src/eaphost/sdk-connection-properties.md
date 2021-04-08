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
# <a name="sdk-connection-properties"></a><span data-ttu-id="7665f-104">SDK-Verbindungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7665f-104">SDK Connection Properties</span></span>

<span data-ttu-id="7665f-105">Bei diesem Beispiel handelt es sich um eine Instanz des nativen [eaphostconfig](eaphostconfigschema-schema.md) -Schemas.</span><span class="sxs-lookup"><span data-stu-id="7665f-105">This sample is an instance of the [eaphostconfig](eaphostconfigschema-schema.md) native schema.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7665f-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7665f-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7665f-107">Verbindungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7665f-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="7665f-108">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="7665f-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




