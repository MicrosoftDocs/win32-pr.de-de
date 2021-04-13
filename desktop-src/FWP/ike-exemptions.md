---
title: IKE-/AuthIP-Ausnahmen
description: Internetschlüsselaustausch (IKE) und authentifiziertes Internetprotokoll (AuthIP) müssen den Netzwerk Datenverkehr von der IPSec-Filterung ausschließen, damit Sie funktionieren.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389932"
---
# <a name="ikeauthip-exemptions"></a>IKE-/AuthIP-Ausnahmen

Die IPSec (Internet Protocol Security)-Schlüssel Bindungs Internetschlüsselaustausch Module (Internet Protocol Security, IKE) und authentifiziertes Internetprotokoll (AuthIP) müssen den Netzwerk Datenverkehr von der IPSec-Filterung ausschließen, damit Sie funktionieren.

In der Windows-Filter Plattform (WFP) fügt das Basis Filtermodul (BFE) automatisch IKE-und AuthIP-Ausnahme Filter hinzu, wenn der erste IKE-oder AuthIP-hauptmodusrichtlinienfilter hinzugefügt wird, und löscht diese, wenn der letzte IKE-oder AuthIP mm-Richtlinien Filter gelöscht wird. Auf diese Weise müssen die Richtlinien Anbieter nicht die IKE-und AuthIP-Filter Ausnahmen einzeln verwalten.

Ein IKE mm-Richtlinien Filter ist ein Filter in der-Engine-Schicht der [**swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , die auf einen Anbieter Kontext vom Typ " [**swpm \_ IPSec \_ IKE \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)" verweist.

Ein AuthIP mm-Richtlinien Filter ist ein Filter in der-Engine-Schicht der [**swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , die auf einen Anbieter Kontext vom Typ " [**swpm \_ IPSec \_ AuthIP \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)" verweist.

Ein IKE-oder AuthIP-Ausnahme Filter ist ein Filter in der-Engine-Schicht für den [**\_ eingehenden \_ \_ Transport \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) oder den **ausgehenden \_ \_ \_ Transport \_ v {4 \| 6** }, der sich im Bereich der [**\_ \_ \_ IKE- \_ Ausnahmen**](filter-weight-identifiers.md) für den Bereich für den schwere Bereich von swpm befindet.

Die von BFE implementierten IKE-und AuthIP-Ausnahmen lauten wie folgt.

| IP-Version      | Port                        | Ausnahme                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP: 500 UDP: 4500<br/> | Erlauben Sie IKE-und AuthIP-Datenverkehr auf der eingehenden Transportschicht und der ausgehenden Transportschicht. <br/> Hiermit wird der IKE-und AuthIP-Datenverkehr auf der ALE Empfangs-/Accept-und Connect-Schicht zugelassen, aber auf das lokale System beschränkt.<br/> |
| IPv6<br/> | UDP: 500<br/>          | Erlauben Sie IKE-und AuthIP-Datenverkehr auf der eingehenden Transportschicht und der ausgehenden Transportschicht. <br/> Hiermit wird der IKE-und AuthIP-Datenverkehr auf der ALE Empfangs-/Accept-und Connect-Schicht zugelassen, aber auf das lokale System beschränkt.<br/> |



 

Die IKE-und AuthIP-Ausnahme Filter sind für alle Adressen offen. Zum Implementieren einer Firewall mit präziserer Kontrolle sollten Richtlinien Anbieter Filter in einem Gewichtungs Bereich hinzufügen, der höher als der [**fwpm- \_ Gewichtungs \_ Bereich von \_ IKE- \_ Ausnahmen**](filter-weight-identifiers.md)ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPSec-Konfiguration](ipsec-configuration.md)
</dt> <dt>

[Filtergewichtungszuweisung](filter-weight-assignment.md)
</dt> </dl>

 

 





