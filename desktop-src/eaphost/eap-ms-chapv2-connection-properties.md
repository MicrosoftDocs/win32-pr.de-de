---
title: EAPMS-CHAPv2 Verbindungseigenschaften
description: Erfahren Sie mehr über die EAPMS-CHAPv2 Verbindungseigenschaften. Sehen Sie sich ein Beispiel an, das eine Instanz des Legacyschemas mschapv2connectionpropertiesv1 ist.
ms.assetid: d6a057e0-56f6-4a31-9391-fde631ac2898
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ec894f8e95aa08e68aae418ed2b194c02a90cd008b9ac8d810d3c497e76f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984260"
---
# <a name="eap-ms-chapv2-connection-properties"></a>EAPMS-CHAPv2 Verbindungseigenschaften

Dieses Beispiel ist eine Instanz des [Legacyschemas mschapv2connectionpropertiesv1.](mschapv2connectionpropertiesv1schema-schema.md)

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>26</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
      xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>26</baseEap:Type> 
        <msChapV2:EapType>
        <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
        </msChapV2:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungseigenschaften](connection-profiles.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> </dl>

 

 




