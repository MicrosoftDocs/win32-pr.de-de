---
title: IKE/AuthIP-Ausnahmen
description: Internetschlüssel-Exchange (IKE) und Authentifiziertes Internetprotokoll (AuthIP) müssen ihren Netzwerkdatenverkehr von der IPsec-Filterung ausgenommen, damit sie funktionieren.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2963c804c6bd63f191563566bcc99dcf9f0f4a74bb2c844a402adc856dbad3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069060"
---
# <a name="ikeauthip-exemptions"></a>IKE/AuthIP-Ausnahmen

Die IPsec-Schlüsselingmodule (Internet Protocol Security, Internetprotokollsicherheit), IKE (Internet Key Exchange) und Authentifiziertes Internetprotokoll (AuthIP) müssen ihren Netzwerkdatenverkehr von der IPsec-Filterung ausgenommen.

In Windows Filtering Platform (WFP) fügt die Basisfilter-Engine (Base Filtering Engine, BFE) automatisch IKE- und AuthIP-Ausnahmefilter hinzu, wenn der erste Richtlinienfilter für den IKE- oder AuthIP-Hauptmodus (MM) hinzugefügt und gelöscht wird, wenn der letzte IKE- oder AuthIP MM-Richtlinienfilter gelöscht wird. Auf diese Weise müssen die Richtlinienanbieter IKE- und AuthIP-Filterausnahmen nicht einzeln verwalten.

Ein IKE MM-Richtlinienfilter ist ein Filter in der Engine-Schicht [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6},**](management-filtering-layer-identifiers-.md) der auf einen Anbieterkontext vom Typ [**FWPM \_ IPSEC \_ IKE \_ MM CONTEXT \_ verweist.**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)

Ein AuthIP MM-Richtlinienfilter ist ein Filter in der Engine-Schicht [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6},**](management-filtering-layer-identifiers-.md) der auf einen Anbieterkontext vom Typ [**FWPM \_ IPSEC \_ AUTHIP \_ MM CONTEXT \_ verweist.**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)

Ein IKE- oder AuthIP-Ausnahmefilter ist ein Filter in der Engine-Schicht [**FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) oder **FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}** automatisch gewichtet im [**FWPM-Gewichtungsbereich \_ \_ \_ \_ IKE-AUSNAHMEN Gewichtungsbereich.**](filter-weight-identifiers.md)

Die von BFE implementierten IKE- und AuthIP-Ausnahmen lauten wie folgt.

| IP-Version      | Port                        | Ausnahme                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP:500 UDP:4500<br/> | Lassen Sie IKE- und AuthIP-Datenverkehr auf der Transportebene für eingehenden Datenverkehr und auf der Transportebene für ausgehenden Datenverkehr zu. <br/> Lassen Sie IKE- und AuthIP-Datenverkehr auf den ALE-Empfangs-/Accept- und Connect-Ebenen zu, beschränken Sie ihn jedoch auf das lokale System.<br/> |
| IPv6<br/> | UDP:500<br/>          | Lassen Sie IKE- und AuthIP-Datenverkehr auf der Transportebene für eingehenden Datenverkehr und auf der Transportebene für ausgehenden Datenverkehr zu. <br/> Lassen Sie IKE- und AuthIP-Datenverkehr auf den ALE-Empfangs-/Accept- und Connect-Ebenen zu, beschränken Sie ihn jedoch auf das lokale System.<br/> |



 

Die IKE- und AuthIP-Ausnahmefilter sind für alle Adressen offen. Um eine Firewall mit präziserer Steuerung zu implementieren, sollten Richtlinienanbieter Filter in einem Gewichtungsbereich hinzufügen, der höher als [**FWPM \_ WEIGHT \_ RANGE \_ \_ IKE-AUSNAHMEN ist.**](filter-weight-identifiers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPsec-Konfiguration](ipsec-configuration.md)
</dt> <dt>

[Filtergewichtungszuweisung](filter-weight-assignment.md)
</dt> </dl>

 

 





