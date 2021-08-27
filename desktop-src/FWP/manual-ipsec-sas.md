---
title: Manuelle Sa
description: Das IPsec-Richtlinienszenario für die manuelle Sicherheitszuordnung (Manual Security Association, SA) ermöglicht Aufrufern, die integrierten IPsec-Schlüsselmodule (IKE und AuthIP) zu umgehen, indem sie IPsec-SAs direkt angeben, um jeglichen Netzwerkdatenverkehr zu schützen.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cdb3d7c67d9cfa513cbdff846c02fd6ba61ebf031672fb86887bc01c90455b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083320"
---
# <a name="manual-sa"></a>Manuelle Sa

Das IPsec-Richtlinienszenario für die manuelle Sicherheitszuordnung (Manual Security Association, SA) ermöglicht Aufrufern, die integrierten IPsec-Schlüsselmodule (IKE und AuthIP) zu umgehen, indem sie IPsec-SAs direkt angeben, um jeglichen Netzwerkdatenverkehr zu schützen.

Ein Beispiel für ein mögliches Szenario mit manueller SA ist das Hinzufügen eines IPsec-SA-Paars, um den gesamten Unicastdatenverkehr zwischen den IP-Adressen 1.1.1 & 2.2.2.2 mit Ausnahme von ICMP mithilfe des IPsec-Transportmodus zu schützen.

> [!Note]  
> Die folgenden Schritte müssen auf beiden Computern mit entsprechend festgelegten IP-Adressen ausgeführt werden.

 

Verwenden Sie die folgende WFP-Konfiguration, um dieses Beispiel programmgesteuert zu implementieren.

<dl>

**Richten Sie auf FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 6} Regeln für \| die Filterung eingehender Pakete ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ LOKALE \_ \_ IP-ADRESSE DER FWPM-BEDINGUNG**                           | Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).           |
    | **IP-REMOTEADRESSE DER \_ \_ FWPM-BEDINGUNG \_ \_**                          | Die entsprechende Remoteadresse (1.1.1.1 oder 2.2.2.2).          |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                         |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**         |

        
2.  Ausschließen von ICMP-Datenverkehr von IPsec durch Hinzufügen eines Filters mit den folgenden Eigenschaften. 

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ ICMP{V6}** Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | [**\_ \_ IKE-AUSNAHMEN FÜR DEN FWPM-GEWICHTUNGSBEREICH \_ \_**](filter-weight-identifiers.md)  |

        

**Richten Sie auf der FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V{4 6} Regeln für \| die Filterung ausgehender Daten pro Paket ein.**  

1.  Fügen Sie einen Filter mit den folgenden Eigenschaften hinzu. 

    | Filter-Eigenschaft                                                   | Wert                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                            |
    | **FWPM \_ BEDINGUNG \_ IP \_ LOCAL \_ ADDRESS** filtering condition       | Die entsprechende lokale Adresse (1.1.1.1 oder 2.2.2.2).    |
    | **FWPM \_ BEDINGUNG \_ IP \_ REMOTE \_ ADDRESS** Filterungsbedingung      | Die entsprechende Remoteadresse (1.1.1.1 oder 2.2.2.2).   |
    | **action.type**                                                   | **\_FWP-AKTIONSAUFRUF \_ \_ BEENDET**                  |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ AUSGEHENDER \_ TRANSPORT \_ V{4 \| 6}** |

        
2.  Ausschließen von ICMP-Datenverkehr von IPsec durch Hinzufügen eines Filters mit den folgenden Eigenschaften. 

    | Filter-Eigenschaft                                                   | Wert                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ BEDINGUNG \_ IP LOCAL ADDRESS \_ \_ \_ TYPE** Filterbedingung | NlatUnicast                                                                |
    | **FWPM \_ BEDINGUNG \_ IP \_ PROTOCOL** Filterungsbedingung             | **IPPROTO \_ ICMP{V6}** Diese Konstanten werden in winsock2.h definiert.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **\_ \_ IKE-AUSNAHMEN FÜR DEN FWPM-GEWICHTUNGSBEREICH \_ \_**                                   |

        

**Einrichten von Eingangs- und Ausgangssicherheitszuordnungen**

1.  Rufen Sie [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)mit dem *Parameter outboundTraffic* auf, der die IP-Adressen als 1.1.1.1 & 2.2.2.2 enthält, und **ipsecFilterId** als LUID des oben hinzugefügten IPsec-Rückruffilters der ausgehenden Transportebene.
2.  Rufen Sie [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)mit dem *ID-Parameter* auf, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und den *Parameter getSpi,* der die IP-Adressen als 1.1.1.1 & 2.2.2.2 enthält, und **ipsecFilterId** als LUID des oben hinzugefügten IPsec-Rückruffilters für eingehende Transportebene. Der zurückgegebene SPI-Wert soll vom lokalen Computer als eingehende SA SPI und vom entsprechenden Remotecomputer als ausgehende SA SPI verwendet werden. Beide Computer müssen einige Out-of-Band-Mittel verwenden, um die SPI-Werte auszutauschen.
3.  Rufen Sie [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)mit dem *ID-Parameter* auf, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *Parameter inboundBundle,* der die Eigenschaften des eingehenden SA-Pakets beschreibt (z. B. die eingehende SA SPI, den Transformationstyp, Algorithmustypen, Schlüssel usw.).
4.  Rufen Sie [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)mit dem *ID-Parameter* auf, der die von [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)zurückgegebene Kontext-ID enthält, und dem *Parameter outboundBundle,* der die Eigenschaften des ausgehenden SA-Pakets beschreibt (z. B. die ausgehende SA SPI, den Transformationstyp, Algorithmustypen, Schlüssel usw.).

  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode: Manuelle SA-Schlüsselung](manual-sa-keying.md)
</dt> <dt>

[**Integrierte Aufrufbezeichner**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

