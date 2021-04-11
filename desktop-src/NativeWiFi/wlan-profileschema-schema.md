---
description: Definiert ein WLAN-Profil, das vom systemeigenen WiFi-AutoConfig-Dienst verwendet wird.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile-Schema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128840"
---
# <a name="wlan_profile-schema"></a>WLAN- \_ Profil Schema

Das WLAN- \_ Profil Schema definiert ein WLAN-Profil, das vom systemeigenen WiFi-AutoConfig-Dienst verwendet wird.

Der AutoConfig-Dienst akzeptiert drahtlos Profile vom Gruppenrichtlinie-Agent, von der Scripting Interface (**netsh**), von der Benutzeroberfläche oder von der USB-Flash-Konfigurationsschnittstelle.

Ein Profil, das von einem dieser Systeme empfangen wird, wird dem WLAN \_ -Profil Schema zugeordnet und im Profil Speicher gespeichert. Profile können mithilfe von Netsh-Befehlen oder mithilfe von API-Elementen wie [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)aus dem Profil Speicher exportiert werden.

Das Stamm Element eines WLAN-Profils ist das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element. Jedes Profil weist genau ein Stamm Element auf. Das **wlanprofile** -Element befindet sich im-Namespace `https://www.microsoft.com/networking/WLAN/profile/v1` .

Beispiel-WLAN-Profile finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

-   [WLAN- \_ Profil Schema Elemente](wlan-profileschema-elements.md)
-   [Einfache Typen von WLAN- \_ Profil Schemas](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netsh-Befehle für WLAN (Wireless Local Area Network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
