---
title: EAP-Attribute
description: Ist eine EAP- \_ Attribut Struktur, die einen vordefinierten Datentyp enthält, der sich auf eine Authentifizierungs Sitzung bezieht.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338701"
---
# <a name="eap-attributes"></a>EAP-Attribute

Ein EAP-Attribut ist eine [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur, die einen vordefinierten Datentyp enthält, der sich auf eine Authentifizierungs Sitzung bezieht. Attribute werden verwendet, um Informationen zwischen EAP-Methoden und Supplicants oder zwischen EAP-Methoden und Authentifikatoren zu übermitteln. Peer-und Authenticator-Implementierungen einer EAP-Methode können diese Attribute über ein Netzwerk austauschen.

Eine komplette Liste der unterstützten Attributtypen wird im Thema [**EAP \_ - \_ Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)angezeigt.

## <a name="attributes-consumed-by-supplicants"></a>Von Supplicants verbrauchte Attribute

Die folgenden Attributtypen werden von 802.1 x-Supplicants genutzt.

-   **eatvendorspecific**

Die folgenden Attributtypen werden von PPP-Client Supplicants genutzt.

-   **eatminimal**
-   **eateaptlv**

Die folgenden Attributtypen werden von PPP-Server Supplicants genutzt.

-   **eatusername**
-   **eatreplymess**
-   **eatstate**
-   **eatsessiontimeout**
-   **eateapmessage**

## <a name="attributes-exported-by-methods"></a>Durch Methoden exportierte Attribute

Die folgenden Attributtypen können von EAP-Methoden exportiert werden.

-   **eatcleartextpassword**
-   **eatquarantinesoh**
-   **eatmethodid**

Der folgende Attributtyp wird von EAP-TLS ( [Transport Level Security](/previous-versions/windows/embedded/ms885336(v=msdn.10)) )-Methoden (EAP-TLS) exportiert.

-   **eatcertifialisieoid**

Die folgenden Attributtypen werden von der [Microsoft Challenge Handshake Authentication Protocol Version 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2)-Methode exportiert.

-   **eatusername**
-   **eatkredentialschge**

Der folgende Attributtyp wird von Netzwerk Richtlinien Server (Network Policy Server, NPS) verwendet.

-   **eatcertifialisieoid**

Die folgenden Attributtypen werden von den [PAP-Methoden (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportiert.

-   **eatusername**
-   **eatapapembeddebug-ID**
-   **eatpinapfastroamedsession**
-   **eatquarantinesoh**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**EAP \_ - \_ Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 