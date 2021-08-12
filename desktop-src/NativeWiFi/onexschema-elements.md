---
description: Ein 802.1X-Profil enthält die folgenden Schemaelemente.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: OneX-Schemaelemente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c20e6bf2b15fa53e5567d02bf3a88135b66fe7de80a171310249ddb941aedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619985"
---
# <a name="onex-schema-elements"></a>OneX-Schemaelemente

Ein 802.1X-Profil enthält die folgenden Schemaelemente. Alle OneX-Schemaelemente gelten sowohl für kabelgebundene als auch für drahtlose Profile. Die meisten benannten Elemente befinden sich im -Namespace, mit Ausnahme von `https://www.microsoft.com/networking/OneX/v1` [**EAPConfig (OneX),**](onexschema-eapconfig-onex-element.md) das sich im Namespace `https://www.microsoft.com/provisioning/EapHostConfig` befindet.

In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden. Die Reihenfolge der Elemente wird erzwungen. Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.

In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem Profil angezeigt werden können, da Elemente in **xs:any-Einfügepunkten hinzugefügt werden** können.

-   [**Onex**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**type (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



