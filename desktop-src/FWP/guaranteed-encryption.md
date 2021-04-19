---
title: Garantierte Verschlüsselung
description: Das Szenario für die garantierte Verschlüsselung der IPSec-Richtlinie erfordert IPSec-Verschlüsselung für den gesamten übereinstimmenden Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314643"
---
# <a name="guaranteed-encryption"></a>Garantierte Verschlüsselung

Das Szenario für die garantierte Verschlüsselung der IPSec-Richtlinie erfordert IPSec-Verschlüsselung für den gesamten übereinstimmenden Diese Richtlinie muss in Verbindung mit einer der Richtlinien Optionen für den Transportmodus angegeben werden.

Die garantierte Verschlüsselung wird normalerweise verwendet, um sensiblen Datenverkehr auf Anwendungs Basis zu verschlüsseln.

Ein Beispiel für ein mögliches verschlüsseltes Verschlüsselungs Szenario ist "Secure all Unicast Data Traffic, außer ICMP, Using IPSec Transport Mode, Enable Aushandlung Discovery, and require eine garantierte Verschlüsselung für den gesamten Unicastdatenverkehr gemäß TCP-Port 5555."

Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.

<dl>

**Auf der swpm- \_ Schicht \_ IKEEXT \_ V {4 \| 6} Einrichten der mm-Aushandlungs Richtlinie**  

1.  Fügen Sie einen oder beide der folgenden mm-Richtlinien Anbieter Kontexte hinzu.  
    -   Für IKE ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ IKE \_ mm \_ context".
    -   Für AuthIP ein Richtlinien Anbieter Kontext vom Typ "swpm \_ IPSec \_ AuthIP \_ mm \_ context".

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

    | Filter-Eigenschaft                                               | Wert                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | Bedingung zum \_ Filtern von \_ lokalen IP- \_ \_ Adress \_ Typen für die Bedingung | [Nlatunicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **Action. Type**                                               | **aufrufende f- \_ Aktions Legende \_ \_**                                                              |
    | **Action. calloutkey**                                         | **Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**                                              |
    | **rawcontext**                                                | [**swpm-Kontext-IPSec-eingehende Beibehaltung der \_ \_ \_ \_ \_ Verbindungs \_ Sicherheit**](filter-context-identifiers.md) |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften.

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
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

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | **IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**                                   |

        

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

        
3.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Dieser Filter lässt nur eingehende Verbindungen mit dem TCP-Port 5555 zu, wenn Sie verschlüsselt sind.

    | Filter-Eigenschaft                                                   | Wert                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                                           |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.<br/>                                    |
    | "F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung          | 5555                                                                                                  |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                                                                 |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec \_ eingehende \_ Initiierung \_ Secure \_ V {4 \| 6}**                                          |
    | **rawcontext**                                                    | [**WPM-Kontext-o- \_ \_ Set- \_ \_ Verbindung \_ erfordert \_ IPSec- \_ Verschlüsselung**](filter-context-identifiers.md) |

        

**Bei der Einrichtung der swpm- \_ Ebene ALE-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6} richten Sie ausgehende Filterregeln pro Verbindung ein.**

-   Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. Mit diesem Filter werden nur ausgehende Verbindungen von TCP-Port 5555 zugelassen, wenn Sie verschlüsselt sind.

    | Filter-Eigenschaft                                                   | Wert                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                                           |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ TCP**: diese Konstante ist in Winsock2. h definiert.<br/>                                    |
    | "F" **\_ Bedingung für die \_ \_ lokale \_ Port** Filterung der Bedingung          | 5555                                                                                                  |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                                                                 |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec- \_ ALE \_ Connect \_ V {4 \| 6}**                                                       |
    | **rawcontext**                                                    | [**WPM-Kontext-o- \_ \_ Set- \_ \_ Verbindung \_ erfordert \_ IPSec- \_ Verschlüsselung**](filter-context-identifiers.md) |

      

  
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

 

