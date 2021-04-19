---
title: Transportmodus
description: Im Transportmodus-IPSec-Richtlinien Szenario ist der IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr erforderlich
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314933"
---
# <a name="transport-mode"></a>Transportmodus

Im Transportmodus-IPSec-Richtlinien Szenario ist der IPSec-Transportmodus für den gesamten übereinstimmenden Datenverkehr erforderlich Alle übereinstimmenden Klartext-Datenverkehr wird gelöscht, bis die IKE-oder AuthIP-Aushandlung erfolgreich abgeschlossen wurde. Wenn die Aushandlung fehlschlägt, bleibt die Konnektivität mit der entsprechenden IP-Adresse beschädigt.

Ein Beispiel für ein mögliches transportmodusszenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode".

Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.

<dl>

**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**  

1.  Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.  
    -   Für IKE ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ IKE \_ mm \_ context**".
    -   Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ mm \_ context**".

    > [!Note]  
    > Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende mm-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providercontextkey** | GUID des in Schritt 1 hinzugefügten mm-Anbieter Kontexts. |

        

**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Setup-und EM-Aushandlungs Richtlinie**  

1.  Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter des-Transportmodus hinzu  
    -   Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".
    -   Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context**". Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.

    > [!Note]  
    > Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providercontextkey** | GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts. |

        

**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | [Nlatunicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **Action. Type**                                                   | aufrufende f- \_ Aktions Legende \_ \_                             |
    | **Action. calloutkey**                                             | Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}             |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                  | Wert                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                               |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung            | Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.<br/>    |
    | **Action. Type**                                                  | f/a- \_ Aktion \_ zulassen                                                       |
    | **weight**                                                       | [**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**](filter-weight-identifiers.md) |

        

**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft                                                   | Wert                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                        |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**              |
    | **Action. calloutkey**                                             | WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6} |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                            |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | f/a- \_ Aktion \_ zulassen                                                    |
    | **weight**                                                        | IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_                                   |

        

</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Transport Modus](using-transport-mode.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Anbieter Kontext Typen**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Filterbedingungen](filtering-conditions.md)
</dt> <dt>

[**\_ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Integrierte Legenden Bezeichner**](built-in-callout-identifiers.md)
</dt> </dl>

 

