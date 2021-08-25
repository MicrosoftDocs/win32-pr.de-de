---
title: SNMPv1-Traptypen (Snmp.h)
description: Die SNMPv1-Traptypen beschreiben einen vordefinierten Satz generischer Traptypen, die so formatiert sind, dass sie dem SNMPv1-Trap-PDU-Standard entsprechen.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7067a6bf5aa1ea11135279484cb74722b8bcc197b507f6bba9b30e35630a2861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886240"
---
# <a name="snmpv1-trap-types"></a>SNMPv1-Traptypen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die SNMPv1-Traptypen beschreiben einen vordefinierten Satz generischer Traptypen, die so formatiert sind, dass sie dem SNMPv1-Trap-PDU-Standard entsprechen.



| Konstante                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | Gibt einen Kaltstartfall an. Der Agent initialisiert Protokollentitäten im verwalteten Modus. Sie kann Objekte in ihrer Ansicht ändern.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | Gibt eine Warmstartfalle an. Der Agent initialisiert sich selbst erneut, ändert jedoch keine Objekte in seiner Ansicht.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | Gibt einen Link-Down-Trap an. Eine angefügte Schnittstelle hat sich vom Nach-oben-Zustand in den Abwärtszustand geändert. Die erste Variable in der Variablenbindungsliste identifiziert die Schnittstelle.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKUP**</dt> </dl>                      | Gibt einen Link-Up-Trap an. Eine angefügte Schnittstelle hat sich vom Start nach unten in den Zustand "Up" geändert. Die erste Variable in der Variablenbindungsliste identifiziert die Schnittstelle.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | Gibt einen Authentifizierungsfehlerfall an. Eine SNMP-Entität hat eine SNMP-Nachricht gesendet, aber fälschlicherweise beansprucht, zu einer bekannten Community zu gehören.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | Gibt eine EGP-Nachbarverlustfalle an. Ein EGP-Peer wurde in den Zustand "Herunter" geändert. Die erste Variable in der Variablenbindungsliste identifiziert die IP-Adresse des EGP-Peers.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERPECIFIC**</dt> </dl> | Gibt einen unternehmensspezifischen Trap an. Es ist ein Ereignis aufgetreten. Sie wird im *specificTrap-Parameter* mit einem unternehmensspezifischen Wert identifiziert.<br/>               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Simple Network Management-Protokoll (SNMP) – Übersicht](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[SNMP-Referenz](snmp-reference.md)
</dt> <dt>

[SNMP-Konstanten](snmp-constants.md)
</dt> </dl>

 

