---
title: EAP-Attribute
description: Eine EAP \_ ATTRIBUTE-Struktur, die einen vordefinierten Datentyp im Zusammenhang mit einer Authentifizierungssitzung enthält.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77898ccde0bbaf9660a7e4c3948cce9ec17d9e4f7773b0900333e7152520c013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117750"
---
# <a name="eap-attributes"></a>EAP-Attribute

Ein EAP-Attribut ist eine [**EAP \_ ATTRIBUTE-Struktur,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) die einen vordefinierten Datentyp im Zusammenhang mit einer Authentifizierungssitzung enthält. Attribute werden verwendet, um Informationen zwischen EAP-Methoden und -Unterstützungen oder zwischen EAP-Methoden und Authentifikatoren zu kommunizieren. Peer- und Authentifikatorimplementierungen einer EAP-Methode können diese Attribute über ein Netzwerk austauschen.

Eine vollständige Liste der unterstützten Attributtypen finden Sie im Thema [**EAP \_ ATTRIBUTE \_ TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Von Suppli überschwungene Attribute

Die folgenden Attributtypen werden von 802.1X-Supplikationen genutzt.

-   **restaurantsVendorSpecific**

Die folgenden Attributtypen werden von CLIENT-Supplikationen verwendet.

-   **restaurantsMinimum**
-   **restaurantsEAPTLV**

Die folgenden Attributtypen werden von SUPPLI-Server-Supplikationen verwendet.

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **sessionSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>Von Methoden exportierte Attribute

Die folgenden Attributtypen können von EAP-Methoden exportiert werden.

-   **restaurantsClearTextPassword**
-   **restaurantsQuarantineSoH**
-   **eatMethodId**

Der folgende Attributtyp wird von EAP [TLS-Methoden (Transport Level Security)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) exportiert.

-   **eatCertificateOID**

Die folgenden Attributtypen werden von [Ms-CHAPv2-Methoden (Microsoft Challenge Handshake Authentication Protocol, Version 2.0)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportiert.

-   **eatUserName**
-   **eatCredentialsChanged**

Der folgende Attributtyp wird vom Netzwerkrichtlinienserver (Network Policy Server, NPS) verwendet.

-   **eatCertificateOID**

Die folgenden Attributtypen werden von [PEAP-Methoden (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportiert.

-   **eatUserName**
-   **restaurantsPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **restaurantsQuarantineSoH**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_EAP-ATTRIBUT**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**\_EAP-ATTRIBUTTYP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 