---
title: Manuelles SA
description: Mit dem IPSec-Richtlinien Szenario "manuelle Sicherheits Zuordnung (SA)" können Aufrufer die integrierten IPsec-Schlüssel Bindungs Module (IKE und AuthIP) umgehen, indem Sie die IPSec-SAS direkt angeben, um den Netzwerkverkehr zu sichern.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314573"
---
# <a name="manual-sa"></a>Manuelles SA

Mit dem IPSec-Richtlinien Szenario "manuelle Sicherheits Zuordnung (SA)" können Aufrufer die integrierten IPsec-Schlüssel Bindungs Module (IKE und AuthIP) umgehen, indem Sie die IPSec-SAS direkt angeben, um den Netzwerkverkehr zu sichern.

Ein Beispiel für ein mögliches Manuelles SA-Szenario ist "Hinzufügen eines IPSec-SA-Paars zum Sichern des gesamten unicastdatenverkehrs zwischen IP-Adressen 1.1.1.1 & 2.2.2.2, mit Ausnahme von ICMP, mit IPSec-Transportmodus".

> [!Note]  
> Die folgenden Schritte müssen auf beiden Computern ausgeführt werden, auf denen die IP-Adressen entsprechend festgelegt sind.

 

Um dieses Beispielprogramm gesteuert zu implementieren, verwenden Sie die folgende WFP-Konfiguration.

<dl>

**Auf der swpm- \_ Schicht \_ eingehender \_ Transport \_ V {4 \| 6} einrichten eingehender Filterregeln pro Paket**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | [Nlatunicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ lokale IP-Adresse der Bedingung für die lokale IP- \_ \_ Adresse**                           | Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).           |
    | **\_ \_ IP-Adresse für die IP- \_ Adresse der Bedingung \_**                          | Die entsprechende Remote Adresse (1.1.1.1 oder 2.2.2.2).          |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                         |
    | **Action. calloutkey**                                             | **Swpm-Legende \_ \_ IPSec- \_ Eingangs \_ Transport \_ V {4 \| 6}**         |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften. 

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | [**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**](filter-weight-identifiers.md)  |

        

**Bei der WPM- \_ Schicht \_ ausgehende \_ Transport \_ V {4 \| 6} Einrichten von ausgehenden Regeln pro Paket Filtern**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                            |
    | "F" **\_ Bedingung für die \_ \_ lokale \_ Adress** Filterung der Bedingung       | Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).    |
    | "F" **\_ Bedingung zum Filtern der Bedingung \_ IP- \_ Remote \_ Adresse**      | Die entsprechende Remote Adresse (1.1.1.1 oder 2.2.2.2).   |
    | **Action. Type**                                                   | **aufrufende f- \_ Aktions Legende \_ \_**                  |
    | **Action. calloutkey**                                             | **WPM-Legende \_ \_ IPSec- \_ ausgehenden \_ Transport \_ V {4 \| 6}** |

        
2.  Ausnehmen von ICMP-Datenverkehr von IPSec durch Hinzufügen eines Filters mit den folgenden Eigenschaften. 

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | "F" **\_ Bedingung für die Filterbedingung für die \_ \_ lokale \_ Adress \_ Typen Bedingung** | Nlatunicast                                                                |
    | "F" **\_ Bedingung für Bedingung \_ -IP- \_ Protokoll** Filterung             | **Ipproto \_ ICMP {V6}** diese Konstanten werden in Winsock2. h definiert.<br/> |
    | **Action. Type**                                                   | **f/a- \_ Aktion \_ zulassen**                                                    |
    | **weight**                                                        | **IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**                                   |

        

**Einrichten von eingehenden und ausgehenden Sicherheits Zuordnungen**

1.  Rufen Sie [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)mit dem Parameter *outboundtraffic* auf, der die IP-Adressen as 1.1.1.1 & 2.2.2.2 und **ipsecfilterid** als LUID des oben hinzugefügten IPSec-Legenden Filters der ausgehenden Transportschicht enthält.
2.  Rufen Sie [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)mit dem *ID* -Parameter auf, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und den *getspi* -Parameter mit den IP-Adressen 1.1.1.1 & 2.2.2.2 und **ipsecfilterid** als LUID des oben hinzugefügten IPSec-Legenden Filters der eingehenden Transportschicht. Der zurückgegebene SPI-Wert ist für die Verwendung als eingehende SA-SPI durch den lokalen Computer und als ausgehende SA-SPI durch den entsprechenden Remote Computer vorgesehen. Beide Computer müssen Out-of-Band-Mittel zum Austauschen der SPI-Werte verwenden.
3.  Aufrufen von [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)mit dem *ID* -Parameter, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *inboundbundle* -Parameter, der die Eigenschaften des eingehenden SA-Bundles beschreibt (z. b. der eingehende SA-SPI, der Transformationstyp, Algorithmustypen, Schlüssel usw.
4.  Aufrufen von [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)mit dem *ID* -Parameter, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *outboundbundle* -Parameter, der die Eigenschaften des ausgehenden SA-Pakets beschreibt (z. b. die ausgehende SA-SPI, der Transformationstyp, Algorithmustypen, Schlüssel usw.).

  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: manuelle SA-Schlüssel Erstellung](manual-sa-keying.md)
</dt> <dt>

[**Integrierte Legenden Bezeichner**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**\_ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

