---
title: SDK-Benutzereigenschaften
description: Erfahren Sie mehr über die SDK-Benutzereigenschaften. Sehen Sie sich ein Beispiel an, bei dem es sich um eine Instanz des nativen eaphustuseranmeldeinformationen
ms.assetid: e8a9656d-48e7-4580-a84d-2b829e7a692f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c8dab154e1ef6c736849720856a23fdfe2e7b3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102487"
---
# <a name="sdk-user-properties"></a>SDK-Benutzereigenschaften

Bei diesem Beispiel handelt es sich um eine Instanz des nativen [eaphustuseranmeldeinschemas](eaphostusercredentialsschema-schema.md) .

``` syntax
  <?xml version="1.0" ?>  
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod> 
    <Credentials>
      <EapType>40</EapType> 
      <Identity>test</Identity> 
      <Password>test</Password> 
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzereigenschaften](user-profiles.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> </dl>

 

 




