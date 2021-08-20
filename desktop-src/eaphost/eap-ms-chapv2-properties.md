---
title: EAP MS-CHAPv2-Benutzereigenschaften
description: Erfahren Sie mehr über die EAP-MS-CHAPv2 Benutzereigenschaften. Sehen Sie sich ein Beispiel an, das eine Instanz des Legacyschemas mschapv2userpropertiesv1 ist.
ms.assetid: f360913d-be5d-4ef0-96c9-652e4d08d9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334405e8c06105f3396ad533138128666421ba51b4c514f4a0bd99f9b9caa30a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086579"
---
# <a name="eap-ms-chapv2-user-properties"></a>EAP MS-CHAPv2-Benutzereigenschaften

Dieses Beispiel ist eine Instanz des Legacyschemas [mschapv2userpropertiesv1.](mschapv2userpropertiesv1schema-schema.md)

``` syntax
<?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
   <EapMethod>
     <eapCommon:Type>26</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1" 
     xmlns:MsChapV2="https://www.microsoft.com/provisioning/MsChapV2UserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>26</baseEap:Type> 
       <MsChapV2:EapType>
         <MsChapV2:Username>test</MsChapV2:Username> 
         <MsChapV2:Password>test</MsChapV2:Password> 
         <MsChapV2:LogonDomain>ias-domain</MsChapV2:LogonDomain> 
       </MsChapV2:EapType>
     </baseEap:Eap>
   </Credentials>
 </EapHostUserCredentials>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzereigenschaften](user-profiles.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> </dl>

 

 




