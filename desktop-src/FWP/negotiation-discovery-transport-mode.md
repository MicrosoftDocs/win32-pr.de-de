---
title: Transport Modus für Aushandlungs Ermittlung
description: Das Szenario für das Aushandeln von Aushandlungs Ermittlungs-Transportmodus erfordert IPSec-Transportmodus für den gesamten eingehenden eingehenden Datenverkehr und fordert den IPSec-Schutz für den Abgleich des ausgehenden Datenverkehrs
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314813"
---
# <a name="negotiation-discovery-transport-mode"></a>Transport Modus für Aushandlungs Ermittlung

Das Szenario für das Aushandeln von Aushandlungs Ermittlungs-Transportmodus erfordert IPSec-Transportmodus für den gesamten eingehenden eingehenden Datenverkehr und fordert den IPSec-Schutz für den Abgleich des ausgehenden Datenverkehrs Daher können ausgehende Verbindungen auf Clear-Text zurückgreifen, wenn eingehende Verbindungen nicht bestehen.

Wenn der Host Computer mit dieser Richtlinie versucht, eine neue ausgehende Verbindung herzustellen, und keine IPSec-SA vorhanden ist, die mit dem Datenverkehr übereinstimmt, sendet der Host die Pakete gleichzeitig als Klartext und startet eine IKE-oder AuthIP-Aushandlung. Wenn die Aushandlung erfolgreich ist, wird die Verbindung auf IPSec-Protected aktualisiert. Andernfalls bleibt die Verbindung Klartext. Wenn IPSec-geschützt ist, kann eine Verbindung nie auf Klartext herabgestuft werden.

Der Transport Modus für die Aushandlung von Aushandlungen wird in der Regel in Umgebungen verwendet, die IPsec-fähige und nicht-IPsec-fähige Computer enthalten.

Ein Beispiel für ein mögliches Aushandlungs Ermittlungs-transportmodusszenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode und enable Aushandlung Discovery".

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

        

**Auf der swpm- \_ Ebene \_ IPSec \_ V {4 \| 6} Einrichten der hoch skalierungsrichtlinie und der EM-Aushandlungs Richtlinie**  

1.  Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie die [**IPSec-Richtlinienflag \_ \_ \_ nd \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.  
    -   Für IKE ein Richtlinien Anbieter Kontext vom Typ "WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport Kontext" \_ .
    -   Für AuthIP ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context". Dieser Kontext kann optional die Richtlinie "AuthIP Extended Mode" (EM) aushandeln enthalten.

    > [!Note]  
    > Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providercontextkey** | GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts. |

        

**Auf der WPM- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} richten Sie eingehende Filterregeln pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | [Nlatunicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                                                              |
    | **Action. calloutkey**                                             | **Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**                                              |
    | **rawcontext**                                                    | [**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**](filter-context-identifiers.md) |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | [**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**](filter-weight-identifiers.md)  |

        

**Auf der WPM- \_ Schicht der \_ ausgehende \_ Transport \_ V {4 \| 6} richten Sie ausgehende Filterregeln pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft                                                   | Wert                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                               |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                                                     |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**                                    |
    | **rawcontext**                                                    | [**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**](filter-context-identifiers.md) |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | **IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**                                   |

        

**Legen Sie auf der swpm- \_ Schicht \_ ALE Authentifizierung \_ \_ \_ \_ V {4 \| 6} eingehende Filterregeln pro Verbindung fest.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt nur eingehende Verbindungsversuche zu, wenn Sie durch IPSec gesichert werden. 

    | Filter-Eigenschaft                                                   | Wert                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                  |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                        |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}** |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | **IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**                                   |

        

</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Transport Modus](using-transport-mode.md)
</dt> <dt>

[ALE Ebenen](ale-layers.md)
</dt> <dt>

[**Integrierte Legenden Bezeichner**](built-in-callout-identifiers.md)
</dt> <dt>

[Filterbedingungen](filtering-conditions.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**\_ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Kontexttyp des WPM- \_ Anbieters \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

