---
title: Remote Identitäts Autorisierung
description: Das Szenario der IPSec-Richtlinie für die Remote Identitäts Autorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remote Sicherheits Prinzipale stammen, die in einer Zugriffs Steuerungs Liste (ACL) der Windows-Sicherheits Beschreibung (SD) angegeben sind.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44022c9696dec25e709d9ab1e374ada295893ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390166"
---
# <a name="remote-identity-authorization"></a>Remote Identitäts Autorisierung

Das Szenario der IPSec-Richtlinie für die Remote Identitäts Autorisierung erfordert, dass eingehende Verbindungen von einem bestimmten Satz von Remote Sicherheits Prinzipale stammen, die in einer Zugriffs Steuerungs Liste (ACL) der Windows-Sicherheits Beschreibung (SD) angegeben sind. Wenn die Remote Identität (wie von IPSec festgelegt) nicht mit der Gruppe zulässiger Identitäten identisch ist, wird die Verbindung gelöscht. Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.

Wenn AuthIP aktiviert ist, können zwei Sicherheits Deskriptoren angegeben werden: eine, die dem AuthIP-Hauptmodus entspricht, und die andere, die dem erweiterten AuthIP-Modus entspricht.

Ein Beispiel für einen möglichen Aushandlungs Ermittlungs-transportmodusszenario ist "Secure all Unicast Data Traffic, mit Ausnahme von ICMP, der IPSec-Transport Modus, die Aushandlung von Aushandlungen aktivieren und den eingehenden Zugriff auf Remote Identitäten beschränken, die gemäß dem IKE/AuthIP-Hauptmodus und dem Sicherheits Deskriptor SD2 (entsprechend dem erweiterten AuthIP-Modus) zulässig sind, gilt für sämtlichen Unicastdatenverkehr, der dem lokalen TCP-Port 5555 entspricht.

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

1.  Fügen Sie einen oder beide der folgenden Einstellungen für den Transportmodus-Richtlinien Anbieter hinzu, und legen Sie die [**IPSec-Richtlinienflag \_ \_ \_ nd \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) fest.  
    -   Für IKE ein Richtlinien Anbieter Kontext vom Typ " **WPM- \_ IPSec- \_ IKE- \_ Quadrat- \_ Transport \_ Kontext**".
    -   Für AuthIP ein Richtlinien Anbieter Kontext vom Typ " **swpm \_ IPSec \_ AuthIP \_ qm \_ Transport \_ context** ", der die Richtlinie für die Richtlinie "AuthIP Extended Mode (EM)" enthält.

    > [!Note]  
    > Ein gängiges Schlüssel Anstellungs Modul wird ausgehandelt, und die entsprechende hoch Richtlinie wird angewendet. AuthIP ist das bevorzugte Schlüsselmodul, wenn sowohl IKE als auch AuthIP unterstützt werden.

     

2.  Fügen Sie für jeden der in Schritt 1 hinzugefügten Kontexte einen Filter mit den folgenden Eigenschaften hinzu. 
    | Filter-Eigenschaft        | Wert                                            |
    |------------------------|--------------------------------------------------|
    | Filterbedingungen   | Leer. Der gesamte Datenverkehr entspricht dem Filter.        |
    | **providercontextkey** | GUID des in Schritt 1 hinzugefügten ESDS-Anbieter Kontexts. |

        

**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**  

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
    | **Action. Type**                                                   | f/a- \_ Aktion \_ zulassen                                                        |
    | **weight**                                                        | [**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**](filter-weight-identifiers.md)  |

        

**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 
    | Filter-Eigenschaft                                                   | Wert                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                               |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                                                     |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}**                                    |
    | **rawcontext**                                                    | [**WPM- \_ Kontext- \_ IPSec \_ ausgehende \_ Aushandlungs Aushandlung \_ ermitteln**](filter-context-identifiers.md) |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften. 
    | Filter-Eigenschaft                                                   | Wert                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                            |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | Ipproto \_ ICMP {V6} diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                |
    | **weight**                                                        | **IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**                               |

        

**Auf dem swpm-Schicht-e/a-Abbild \_ \_ \_ \_ \_ akzeptieren \_ V {4 \| 6} eingehende Filterregeln für eingehende Verbindungen pro Verbindung**  

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

        
3.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt eingehende Verbindungen mit dem TCP-Port 5555 zu, wenn die entsprechenden Remote Identitäten sowohl von SD1 als auch von SD2 zugelassen werden. 
    | Filter-Eigenschaft                                                   | Wert                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                        |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.<br/> |
    | "F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung          | 5555                                                               |
    | **fwpm-Bedingungs- \_ \_ ID- \_ Remote Computer- \_ \_ ID**                     | SD1                                                                |
    | **\_ \_ \_ Remote \_ Benutzer- \_ ID der swpm-Bedingungs-ALE**                        | SD2                                                                |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                              |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**       |

        
4.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter blockiert alle anderen eingehenden Verbindungen mit dem TCP-Port 5555, die nicht dem vorherigen Filter entsprechen. 
    | Filter-Eigenschaft                                                   | Wert                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                        |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.<br/> |
    | "F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung          | 5555                                                               |
    | **Action. Type**                                                   | **f- \_ Aktions \_ Block**                                             |

        

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

 

