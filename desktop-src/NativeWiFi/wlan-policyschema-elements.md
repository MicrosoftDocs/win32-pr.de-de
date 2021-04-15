---
description: Ein System eigenes WLAN-Richtlinien Profil besteht aus den folgenden Schema Elementen.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Schema Elemente WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525763"
---
# <a name="wlan_policy-schema-elements"></a>Schema Elemente für WLAN- \_ Richtlinien

Ein System eigenes WLAN-Richtlinien Profil besteht aus den folgenden Schema Elementen. Alle benannten Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WLAN/policy/v1` .

In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden. Die Reihenfolge der Elemente wird erzwungen. Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.

In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem Profil angezeigt werden können, da Elemente in **xs: beliebige** Einfügepunkte hinzugefügt werden können.

-   [**Wlanpolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**Name (wlanpolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Beschreibung (wlanpolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalflags (wlanpolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableautoconfig (globalflags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showdeniednetwork (globalflags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**' zugweveryonetoken ' (globalflags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**Network Filter (wlanpolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**AllowList (NetworkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**Netzwerk (AllowList)**](wlan-policyschema-network-allowlist-element.md)
                -   [**Network Name (networkitemtype)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**NetworkType (networkitemtype)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**blocklist (NetworkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**Netzwerk (blocklist)**](wlan-policyschema-network-blocklist-element.md)
                -   [**Network Name (networkitemtype)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**NetworkType (networkitemtype)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyallibss (NetworkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyalless (NetworkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**ProfileList (wlanpolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



