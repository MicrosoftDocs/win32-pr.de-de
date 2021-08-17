---
title: Garantierte Verschlüsselung
description: Das IPsec-Richtlinienszenario für die garantierte Verschlüsselung erfordert IPsec-Verschlüsselung für den gesamten übereinstimmenden Datenverkehr. Diese Richtlinie muss in Verbindung mit einer der Transportmodus-Richtlinienoptionen angegeben werden.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d029b3bebc6fc6e0a438c5123bb6703bc45dd457195fa7ff8fc7268bba16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069150"
---
# <a name="guaranteed-encryption"></a>Garantierte Verschlüsselung

Das IPsec-Richtlinienszenario für die garantierte Verschlüsselung erfordert IPsec-Verschlüsselung für den gesamten übereinstimmenden Datenverkehr. Diese Richtlinie muss in Verbindung mit einer der Transportmodus-Richtlinienoptionen angegeben werden.

Die garantierte Verschlüsselung wird in der Regel verwendet, um sensiblen Datenverkehr pro Anwendung zu verschlüsseln.

Ein Beispiel für ein mögliches Szenario für die garantierte Verschlüsselung ist "Sichern des gesamten Unicastdatenverkehrs mit Ausnahme von ICMP, Verwenden des IPsec-Transportmodus, Aktivieren der Aushandlungsermittlung und Erfordern einer garantierten Verschlüsselung für den gesamten Unicastdatenverkehr, der dem lokalen TCP-Port 5555 entspricht".

Verwenden Sie die folgende WFP-Konfiguration, um dieses Beispiel programmgesteuert zu implementieren.

<dl>

**Richten Sie auf FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} die MM-Aushandlungsrichtlinie ein.**  

1.  Fügen Sie einen oder beide der folgenden MM-Richtlinienanbieterkontexte hinzu.  
    -   Bei IKE ein Richtlinienanbieterkontext vom Typ FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT.
    -   Bei AuthIP ein Richtlinienanbieterkontext vom Typ FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT.

    > [!Note]  
    > Ein gemeinsames Schlüsselmodul wird ausgehandelt, und die entsprechende MM-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providerContextKey** | GUID des mm-Anbieterkontexts, der in Schritt 1 hinzugefügt wurde. |

        

**Einrichten der \_ QM- und EM-Aushandlungsrichtlinie auf FWPM LAYER \_ IPSEC \_ \| V{4 6}**  

1.  Fügen Sie einen oder beide der folgenden Richtlinienanbieterkontexte für den QM-Transportmodus hinzu, und legen Sie das [**\_ FLAG IPSEC POLICY FLAG \_ \_ ND SECURE \_ fest.**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)  
    -   Für IKE ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ IKE \_ QM TRANSPORT \_ \_ CONTEXT**.
    -   Bei AuthIP ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ AUTHIP \_ QM TRANSPORT \_ \_ CONTEXT**. Dieser Kontext kann optional die EM-Aushandlungsrichtlinie (Extended Mode, erweiterter AuthIP-Modus) enthalten.

    > [!Note]  
    > Ein gemeinsames Schlüsselmodul wird ausgehandelt, und die entsprechende QM-Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providerContextKey** | GUID des in Schritt 1 hinzugefügten QM-Anbieterkontexts. |

        

**Richten Sie auf FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 6} Regeln für \| die Filterung eingehender Pakete ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                               | Wert                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | Filterbedingung für \_ FWPM-BEDINGUNG IP LOCAL ADDRESS \_ \_ \_ \_ TYPE | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                               | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                                                              |
    | **action.calloutKey**                                         | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**                                              |
    | **rawContext**                                                | [**VERBINDUNGSSICHERHEIT FÜR EINGEHENDEN \_ \_ IPSEC-KONTEXT DES FWPM-KONTEXTS \_ \_ \_ \_**](filter-context-identifiers.md) |

        
2.  Ausschließen von ICMP-Datenverkehr von IPsec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ ICMP{V6}** Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | [**\_ \_ IKE-AUSNAHMEN FÜR DEN FWPM-GEWICHTUNGSBEREICH \_ \_**](filter-weight-identifiers.md)  |

        

**Richten Sie auf der FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 6} Regeln für \| die Filterung ausgehender Daten pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu.

    | Filter-Eigenschaft                                                   | Wert                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                               |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ AUSGEHENDER \_ TRANSPORT \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**ERMITTLUNG DER \_ \_ \_ AUSGEHENDEN IPSEC-AUSHANDLUNG \_ IM FWPM-KONTEXT \_**](filter-context-identifiers.md) |

        
2.  Ausschließen von ICMP-Datenverkehr von IPsec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ ICMP{V6}** Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **\_ \_ IKE-AUSNAHMEN FÜR DEN FWPM-GEWICHTUNGSBEREICH \_ \_**                                   |

        

**Richten Sie auf FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} ein, um Filterregeln für eingehende Verbindungen pro Verbindung einzurichten.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt eingehende Verbindungsversuche nur zu, wenn sie durch IPsec geschützt sind. 

    | Filter-Eigenschaft                                                   | Wert                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                  |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V{4 \| 6}** |

        
2.  Ausschließen von ICMP-Datenverkehr von IPsec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ ICMP{V6}** Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **\_ \_ IKE-AUSNAHMEN FÜR DEN FWPM-GEWICHTUNGSBEREICH \_ \_**                                   |

        
3.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt nur eingehende Verbindungen mit TCP-Port 5555 zu, wenn sie verschlüsselt sind.

    | Filter-Eigenschaft                                                   | Wert                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                                           |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ TCP** Diese Konstante ist in winsock2.h definiert.<br/>                                    |
    | **FWPM \_ BEDINGUNG IP LOCAL PORT filtering condition \_ (BEDINGUNGS-IP \_ LOCAL PORT-Filterbedingung) \_**          | 5555                                                                                                  |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                                                                 |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V{4 \| 6}**                                          |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ ENCRYPTION**](filter-context-identifiers.md) |

        

**Richten Sie auf FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6} Filterregeln für ausgehende Verbindungen pro Verbindung ein.**

-   Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt ausgehende Verbindungen von TCP-Port 5555 nur zu, wenn sie verschlüsselt sind.

    | Filter-Eigenschaft                                                   | Wert                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                                           |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ TCP** Diese Konstante ist in winsock2.h definiert.<br/>                                    |
    | **FWPM \_ BEDINGUNG IP LOCAL PORT filtering condition \_ (BEDINGUNGS-IP \_ LOCAL PORT-Filterbedingung) \_**          | 5555                                                                                                  |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                                                                 |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V{4 \| 6}**                                                       |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ ENCRYPTION**](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Verwenden des Transportmodus](using-transport-mode.md)
</dt> <dt>

[ALE-Ebenen](ale-layers.md)
</dt> <dt>

[**Integrierte Aufrufbezeichner**](built-in-callout-identifiers.md)
</dt> <dt>

[Filterbedingungen](filtering-conditions.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_FWPM-ANBIETERKONTEXTTYP \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

