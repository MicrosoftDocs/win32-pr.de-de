---
title: Transportmodus der Aushandlungsermittlung
description: Das IPsec-Richtlinienszenario für den Aushandlungsermittlungs-Transportmodus erfordert IPsec-Transportmodusschutz für den entsprechenden eingehenden Datenverkehr und fordert IPsec-Schutz für den Abgleich von ausgehenden Datenverkehr an.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990a7f84e20d081933ffa0def9800ff7610a3a0e3a6d01dd3b45fe7c99729ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102140"
---
# <a name="negotiation-discovery-transport-mode"></a>Transportmodus der Aushandlungsermittlung

Das IPsec-Richtlinienszenario für den Aushandlungsermittlungs-Transportmodus erfordert IPsec-Transportmodusschutz für den entsprechenden eingehenden Datenverkehr und fordert IPsec-Schutz für den Abgleich von ausgehenden Datenverkehr an. Daher dürfen ausgehende Verbindungen ein Fallback auf Klartext verwenden, eingehende Verbindungen nicht.

Wenn der Hostcomputer mit dieser Richtlinie versucht, eine neue ausgehende Verbindung herzustellen, und keine vorhandene IPsec-SA vorhanden ist, die mit dem Datenverkehr übereinstimmen soll, sendet der Host die Pakete gleichzeitig als Klartext und startet eine IKE- oder AuthIP-Aushandlung. Wenn die Aushandlung erfolgreich ist, wird die Verbindung auf IPsec-geschützt aktualisiert. Andernfalls bleibt die Verbindung im Klartext. Sobald IPsec geschützt ist, kann eine Verbindung nie auf Klartext herabgestuft werden.

Der Transportmodus der Aushandlungsermittlung wird in der Regel in Umgebungen verwendet, die sowohl IPsec-fähige als auch nicht IPsec-fähige Computer enthalten.

Ein Beispiel für ein mögliches Szenario des Transportmodus für die Aushandlungsermittlung ist "Schützen des ganzen Unicastdatenverkehrs mit Ausnahme von ICMP, Verwenden des IPsec-Transportmodus und Aktivieren der Aushandlungsermittlung".

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

        

**Richten Sie auf der FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} die QM- und EM-Aushandlungsrichtlinie ein.**  

1.  Fügen Sie einen oder beide der folgenden Richtlinienanbieterkontexte für den QM-Transportmodus hinzu, und legen Sie das [**Flag IPSEC \_ POLICY FLAG \_ \_ ND \_ SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.  
    -   Bei IKE ein Richtlinienanbieterkontext vom Typ FWPM \_ IPSEC \_ IKE \_ QM TRANSPORT \_ \_ CONTEXT.
    -   Für AuthIP ein Richtlinienanbieterkontext vom Typ FWPM \_ IPSEC \_ AUTHIP \_ QM TRANSPORT \_ \_ CONTEXT. Dieser Kontext kann optional die Aushandlungsrichtlinie für den erweiterten Authentifizierungsmodus (AuthIP Extended Mode, EM) enthalten.

    > [!Note]  
    > Ein gemeinsames Schlüsselmodul wird ausgehandelt, und die entsprechende QM-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der ganze Datenverkehr wird mit dem Filter übereinstimmen.        |
    | **providerContextKey** | GUID des in Schritt 1 hinzugefügten QM-Anbieterkontexts. |

        

**Richten Sie bei FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} Filterregeln für eingehenden Datenverkehr pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                                   | **FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)**                                                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**                                              |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY**](filter-context-identifiers.md) |

        
2.  Entfernen Sie ICMP-Datenverkehr von IPsec, indem Sie einen Filter mit den folgenden Eigenschaften hinzufügen.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | **IPPROTO \_ ICMP{V6} Diese** Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **\_ \_ FWP-AKTIONSGENEHMIGUNG**                                                    |
    | **weight**                                                        | [**IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_**](filter-weight-identifiers.md)  |

        

**Richten Sie bei FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6} Filterregeln für ausgehenden Datenverkehr pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft                                                   | Wert                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                                               |
    | **action.type**                                                   | **FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**\_FWPM-KONTEXT \_ IPSEC \_ OUTBOUND \_ NEGOTIATE \_ DISCOVER**](filter-context-identifiers.md) |

        
2.  Entfernen Sie ICMP-Datenverkehr von IPsec, indem Sie einen Filter mit den folgenden Eigenschaften hinzufügen.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | **IPPROTO \_ ICMP{V6} Diese** Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **\_ \_ FWP-AKTIONSGENEHMIGUNG**                                                    |
    | **weight**                                                        | **IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_**                                   |

        

**Richten Sie bei FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} Filterregeln für eingehenden Datenverkehr pro Verbindung ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt nur eingehende Verbindungsversuche zu, wenn sie durch IPsec geschützt sind. 

    | Filter-Eigenschaft                                                   | Wert                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                  |
    | **action.type**                                                   | **FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V{4 \| 6}** |

        
2.  Entfernen Sie ICMP-Datenverkehr von IPsec, indem Sie einen Filter mit den folgenden Eigenschaften hinzufügen.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | **IPPROTO \_ ICMP{V6} Diese** Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **\_ \_ FWP-AKTIONSGENEHMIGUNG**                                                    |
    | **weight**                                                        | **IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_**                                   |

        

</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Transportmodus](using-transport-mode.md)
</dt> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[**Integrierte Calloutbezeichner**](built-in-callout-identifiers.md)
</dt> <dt>

[Filterbedingungen](filtering-conditions.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**KONTEXTTYP DES \_ \_ FWPM-ANBIETERS \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

