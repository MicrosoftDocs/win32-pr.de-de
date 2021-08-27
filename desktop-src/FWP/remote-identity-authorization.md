---
title: Remoteidentitätsautorisierung
description: Das IPsec-Richtlinienszenario für die Remoteidentitätsautorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remotesicherheitsprinzipals stammen, die in einer Windows-Sicherheitsbeschreibungs-Zugriffssteuerungsliste (ACL) angegeben sind.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c426f0d153d45d3699020bb723b15d75d84df4662fd0bb61d66513c2af24fe31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075380"
---
# <a name="remote-identity-authorization"></a>Remoteidentitätsautorisierung

Das IPsec-Richtlinienszenario für die Remoteidentitätsautorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remotesicherheitsprinzipals stammen, die in einer Windows-Sicherheitsbeschreibungs-Zugriffssteuerungsliste (ACL) angegeben sind. Wenn die Remoteidentität (wie von IPsec bestimmt) nicht mit dem Satz zulässiger Identitäten übereinstimmen, wird die Verbindung gelöscht. Diese Richtlinie muss in Verbindung mit einer der Richtlinienoptionen für den Transportmodus angegeben werden.

Wenn AuthIP aktiviert ist, können zwei Sicherheitsdeskriptoren angegeben werden: eine für den Hauptmodus AuthIP und eine für den erweiterten AuthIP-Modus.

Ein Beispiel für ein mögliches Szenario für den Aushandlungsermittlungs-Transportmodus ist " Schützen des sämtlichen Unicastdatenverkehrs mit Ausnahme von ICMP mithilfe des IPsec-Transportmodus, Aktivieren der Aushandlungsermittlung und Einschränken des eingehenden Zugriffs auf Remoteidentitäten, die laut Sicherheitsbeschreibung SD1 (entsprechend dem Hauptmodus IKE/AuthIP) zulässig sind, und Sicherheitsbeschreibung SD2 (entsprechend dem erweiterten AuthIP-Modus) für den sämtlichen Unicastdatenverkehr, der dem lokalen TCP-Port 5555 entspricht.

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

1.  Fügen Sie einen oder beide der folgenden Richtlinienanbieterkontexte für den QM-Transportmodus hinzu, und legen Sie das [**Flag IPSEC \_ POLICY FLAG \_ \_ ND \_ SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.  
    -   Bei IKE ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ IKE \_ QM TRANSPORT \_ \_ CONTEXT**.
    -   Bei AuthIP ein Richtlinienanbieterkontext vom Typ **FWPM \_ IPSEC \_ AUTHIP \_ QM TRANSPORT \_ \_ CONTEXT,** der die AUShandlungsrichtlinie für den erweiterten Authentifizierungsmodus (AuthIP Extended Mode, EM) enthält.

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
    | **action.type**                                                   | \_ \_ FWP-AKTIONSGENEHMIGUNG                                                        |
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

    | Filter-Eigenschaft                                                   | Wert                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                            |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | IPPROTO \_ ICMP{V6}Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **\_ \_ FWP-AKTIONSGENEHMIGUNG**                                                |
    | **weight**                                                        | **IKE-AUSNAHMEN \_ \_ FÜR \_ FWPM-GEWICHTUNGSBEREICH \_**                               |

        

**Richten Sie bei FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}-Filterregeln für eingehenden Datenverkehr pro Verbindung ein.**  

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

        
3.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt eingehende Verbindungen mit TCP-Port 5555 zu, wenn die entsprechenden Remoteidentitäten sowohl von SD1 als auch von SD2 zugelassen werden. 

    | Filter-Eigenschaft                                                   | Wert                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                        |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | **IPPROTO \_ TCP** Diese Konstante wird in winsock2.h definiert.<br/> |
    | **FWPM \_ CONDITION IP LOCAL PORT filtering condition \_ (BEDINGUNG: \_ FILTERBEDINGUNG FÜR \_ DEN LOKALEN PORT)**          | 5555                                                               |
    | **\_FWPM-BEDINGUNG \_ – \_ ALE-REMOTECOMPUTER-ID \_ \_**                     | SD1                                                                |
    | **\_ \_ ALE-REMOTEBENUTZER-ID FÜR \_ FWPM-BEDINGUNG \_ \_**                        | SD2                                                                |
    | **action.type**                                                   | **FWP \_ ACTION CALLOUT TERMINATING (FWP-AKTIONSAUFRUF \_ WIRD \_ BEENDET)**                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V{4 \| 6}**       |

        
4.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter blockiert alle anderen eingehenden Verbindungen mit TCP-Port 5555, die nicht mit dem vorherigen Filter übereinstimmen. 

    | Filter-Eigenschaft                                                   | Wert                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG: \_ \_ FILTERbedingung "IP \_ LOCAL ADDRESS \_ TYPE"** | NlatUnicast                                                        |
    | **FWPM \_ BEDINGUNG \_ \_ IP-PROTOKOLL-** Filterbedingung             | **IPPROTO \_ TCP** Diese Konstante wird in winsock2.h definiert.<br/> |
    | **FWPM \_ CONDITION IP LOCAL PORT filtering condition \_ (BEDINGUNG: \_ FILTERBEDINGUNG FÜR \_ DEN LOKALEN PORT)**          | 5555                                                               |
    | **action.type**                                                   | **\_ \_ FWP-AKTIONSBLOCK**                                             |

        

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

 

