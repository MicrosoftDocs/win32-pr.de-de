---
title: Transportmodus
description: Das IPsec-Richtlinienszenario für den Transportmodus erfordert IPsec-Transportmodusschutz für den entsprechenden Datenverkehr.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebfb6dad27340bfc72397307c58fddfe2bdf6eeadb65081faa0e1941de2c052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535890"
---
# <a name="transport-mode"></a>Transportmodus

Das IPsec-Richtlinienszenario für den Transportmodus erfordert IPsec-Transportmodusschutz für den entsprechenden Datenverkehr. Jeder übereinstimmende Klartextdatenverkehr wird gelöscht, bis die IKE- oder AuthIP-Aushandlung erfolgreich abgeschlossen wurde. Wenn die Aushandlung fehlschlägt, bleibt die Verbindung mit der entsprechenden IP-Adresse unterbrochen.

Ein Beispiel für ein mögliches Transportmodusszenario ist "Secure all unicast data traffic, except ICMP, using IPsec transport mode".

Verwenden Sie die folgende WFP-Konfiguration, um dieses Beispiel programmgesteuert zu implementieren.

<dl>

**Richten Sie in FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} die MM-Aushandlungsrichtlinie ein.**  

1.  Fügen Sie einen oder beide der folgenden MM-Richtlinienanbieterkontexte hinzu.  
    -   Bei IKE ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**.
    -   Für AuthIP ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Ein allgemeines Schlüsselmodul wird ausgehandelt, und die entsprechende MM-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der ganze Datenverkehr wird mit dem Filter übereinstimmen.        |
    | **providerContextKey** | GuiD des in Schritt 1 hinzugefügten MM-Anbieterkontexts. |

        

**Richten Sie bei FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} die QM- und EM-Aushandlungsrichtlinie ein.**  

1.  Fügen Sie einen oder beide der folgenden Richtlinienkontexte für den QM-Transportmodus hinzu.  
    -   Bei IKE ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ IKE \_ QM TRANSPORT \_ \_ CONTEXT**.
    -   Für AuthIP ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ AUTHIP \_ QM TRANSPORT \_ \_ CONTEXT**. Dieser Kontext kann optional die Aushandlungsrichtlinie für den erweiterten Authentifizierungsmodus (AuthIP Extended Mode, EM) enthalten.

    > [!Note]  
    > Ein gemeinsames Schlüsselmodul wird ausgehandelt, und die entsprechende QM-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der ganze Datenverkehr wird mit dem Filter übereinstimmen.        |
    | **providerContextKey** | GUID des in Schritt 1 hinzugefügten QM-Anbieterkontexts. |

        

**Richten Sie bei FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} Filterregeln für eingehenden Datenverkehr pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **action.type**                                                   | FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)                             |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}             |

        
2.  Entfernen Sie ICMP-Datenverkehr von IPsec, indem Sie einen Filter mit den folgenden Eigenschaften hinzufügen.

    | Filter-Eigenschaft                                                  | Wert                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                               |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung            | IPPROTO \_ ICMP{V6}Diese Konstanten werden in winsock2.h definiert.<br/>    |
    | **action.type**                                                  | \_ \_ FWP-AKTIONSGENEHMIGUNG                                                       |
    | **weight**                                                       | [**IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_**](filter-weight-identifiers.md) |

        

**Richten Sie bei FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} Filterregeln für ausgehenden Datenverkehr pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft                                                   | Wert                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                        |
    | **action.type**                                                   | **FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)**              |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} |

        
2.  Entfernen Sie ICMP-Datenverkehr von IPsec, indem Sie einen Filter mit den folgenden Eigenschaften hinzufügen.

    | Filter-Eigenschaft                                                   | Wert                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                            |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | IPPROTO \_ ICMP{V6}Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | \_ \_ FWP-AKTIONSGENEHMIGUNG                                                    |
    | **weight**                                                        | IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_                                   |

        

</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Transportmodus](using-transport-mode.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Anbieterkontexttypen**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Filterbedingungen](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Integrierte Calloutbezeichner**](built-in-callout-identifiers.md)
</dt> </dl>

 

