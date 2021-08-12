---
description: Definiert ein WLAN-Profil, das vom Native Wifi AutoConfig-Dienst verwendet wird.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile Schema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619067"
---
# <a name="wlan_profile-schema"></a>\_WLAN-Profilschema

Das \_ WLAN-Profilschema definiert ein WLAN-Profil, das vom Native Wifi AutoConfig-Dienst verwendet wird.

Der AutoConfig-Dienst akzeptiert Drahtlosprofile vom Gruppenrichtlinie-Agent, der Skriptschnittstelle (**netsh**), der Benutzeroberfläche oder von der USB-Flashkonfigurationsschnittstelle.

Ein von einem dieser Systeme empfangenes Profil wird dem WLAN-Profilschema zugeordnet \_ und im Profilspeicher gespeichert. Profile können mit netsh-Befehlen oder api-Elementen wie WlanGetProfile aus dem [**Profilspeicher exportiert werden.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)

Das Stammelement eines WLAN-Profils ist das [**WLANProfile-Element.**](wlan-profileschema-wlanprofile-element.md) Jedes Profil hat genau ein Stammelement. Das **WLANProfile-Element** befindet sich im Namespace `https://www.microsoft.com/networking/WLAN/profile/v1` .

Beispiele für WLAN-Beispielprofile finden Sie unter [Beispiele für Drahtlosprofile.](wireless-profile-samples.md)

-   [\_WLAN-Profilschemaelemente](wlan-profileschema-elements.md)
-   [\_WLAN-Profilschema – einfache Typen](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netsh-Befehle für drahtloses lokales Netzwerk (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
