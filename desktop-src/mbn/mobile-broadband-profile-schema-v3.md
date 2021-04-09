---
description: Mobiles Breitband Profil Schema v3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Mobiles Breitband Profil Schema v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862508"
---
# <a name="mobile-broadband-profile-schema-v3"></a>Mobiles Breitband Profil Schema v3

Das Windows 8mobile-Breitband Profil Schema v3 ist im-Namespace verfügbar `https://www.microsoft.com/networking/WWAN/profile/v3` .

-   [Mobile Breitband Profile Schema V3-Elemente](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



