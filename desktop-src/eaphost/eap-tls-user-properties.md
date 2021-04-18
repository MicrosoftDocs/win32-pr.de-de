---
title: EAP-TLS-Benutzereigenschaften
description: Erfahren Sie mehr über EAP-TLS-Benutzereigenschaften. Sehen Sie sich ein Beispiel an, das eine Instanz des eaptlsuserpropertiesv1-Legacy Schemas ist.
ms.assetid: d5a265a9-4c09-4a60-a188-dff471ee72c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d104d8eb5eaca67985be5574504dfbe57b5a6f9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106340291"
---
# <a name="eap-tls-user-properties"></a><span data-ttu-id="245c7-104">EAP-TLS-Benutzereigenschaften</span><span class="sxs-lookup"><span data-stu-id="245c7-104">EAP-TLS User Properties</span></span>

<span data-ttu-id="245c7-105">Bei diesem Beispiel handelt es sich um eine Instanz des [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) -Legacy Schemas.</span><span class="sxs-lookup"><span data-stu-id="245c7-105">This sample is an instance of the [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) legacy schema.</span></span>

``` syntax
 <?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials"> 
   <EapMethod>
     <eapCommon:Type>13</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsUserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>13</baseEap:Type> 
       <eapTls:EapType>
         <eapTls:Username>ias-domain\test</eapTls:Username> 
         <eapTls:UserCert /> 
       </eapTls:EapType>
     </baseEap:Eap>
   </Credentials>
 </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="245c7-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="245c7-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="245c7-107">Benutzereigenschaften</span><span class="sxs-lookup"><span data-stu-id="245c7-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="245c7-108">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="245c7-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




